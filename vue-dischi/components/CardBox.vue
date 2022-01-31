<template>
  <div>
    <div class="card">
      <img :src="song.poster" alt="" />
      <h1>{{ song.title }}</h1>
      <p>{{ song.author }}</p>
      <p>{{ song.year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    song: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  text-align: center;
  width: calc(170px - 20px);
  margin: 10px 10px;
  flex-direction: column;
  background-color: rgba(255, 255, 255, 0.1);
  padding: 20px  0px;
  height: 280px;

  img {
    width: 100%;
    max-width: 100px;
    margin: 0 auto;
  }

  h1 {
    font-size: 20px;
    max-width: 100px;
    margin: 0 auto;
    margin-top: 10px;
    margin-bottom: 10px;
    color: white;
  }
  p{
      color: gray;
  }
}
</style>