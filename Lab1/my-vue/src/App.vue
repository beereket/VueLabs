<template>
  <!--  <img alt="Vue logo" src="./assets/logo.png">-->
  <!--  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <Header></Header>
  <Main></Main>
</template>

<script>

import Main from "@/components/Main.vue";
import Header from "@/components/Header.vue";

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Main,
    Header,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  margin: 0;
  padding: 0;
}
</style>
