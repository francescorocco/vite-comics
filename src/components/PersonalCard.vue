<script>
export default {
  name: "PersonalCard",
  props:{
    image: String,
    name: String
  }
}
</script>

<template>
  <div class="card">
    <div class="image-wrapper">
      <img :src="image" :alt="name">
    </div>
    <h3>{{ name }}</h3>
  </div>
</template>

<style scoped lang="scss">
  .card{
    width: 200px;
    height: 300px;

    h3{
      color:white;
      text-align: center;
    }

    img{
      width: 200px;
      height: 300px;
    }
  }
</style>