  <script>
    import TheHeader from "./components/TheHeader.vue";
    import TheFooter from "./components/TheFooter.vue";

    export default{
      components:{
        TheHeader,
        TheFooter,
      }
    }
  </script>

<template>

  <TheHeader/>

  <TheFooter/>
</template>

<style lang="scss">
@use "./style/general.scss";

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body{
  font-family: 'Roboto Condensed', sans-serif;
}
</style>