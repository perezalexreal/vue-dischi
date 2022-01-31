<template>
  <div id="app">
    <main-container :listSongs="listSongs"/>
  </div>
</template>

<script>
import axios from 'axios'

import MainContainer from '../components/MainContainer.vue'

export default {
  name: 'App',
  data () {
    return {
      listSongs: []
    }
  },
  components: {
    MainContainer
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.listSongs = result.data.response;
    });
  }
}
</script>

<style lang="scss">
 * {
   padding: 0;
   margin: 0;
   box-sizing: border-box;
   
 }

 body {
   background-color:  #1B365D;
 }
</style>
