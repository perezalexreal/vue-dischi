<template>
<div class="main-container">
  <card-box v-for="(song,index) in listSongs" :key="index" :song="song" />
</div>

</template>

<script>
import CardBox from './CardBox.vue'

export default {
    components: {
        CardBox
    },
    props: {
        listSongs: Array
    }
}
</script>

<style lang="scss" scoped>
 .main-container  {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    width: 100%;
    max-width: 850px;
    margin: 0 auto;
    padding-top: 50px;
    }
</style>