  <script>
    import TheHeader from "./components/TheHeader.vue";
    import TheJumbotron from "./components/TheJumbotrone.vue";
    import TheMain from "./components/TheMain.vue";
    import MyInformationBar from "./components/MyInformationBar.vue";
    import TheFooter from "./components/TheFooter.vue";



    export default{
      components:{
        TheHeader,
        TheJumbotron,
        TheMain,
        MyInformationBar,
        TheFooter
      }
    }
  </script>

<template>

  <TheHeader/>

  <TheJumbotron/>

  <TheMain/>

  <MyInformationBar/>

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