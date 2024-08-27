<template>
  <div id="app">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
<!--    <hello-world msg="Welcome to Your Vue.js App"/>-->
    <basic-element />
  </div>
</template>

<script>
import HelloWorld from '@/views/zero/HelloWorld.vue'
import BasicElement from "@/views/element/basic/BasicElement.vue";

export default {
  name: 'App',
  components: {BasicElement, HelloWorld }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
