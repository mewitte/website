<template>
  <div id="app">
    <Landing backgroundImage="/img/background1.jpg" />
    <About />
  </div>
</template>

<script>
import Landing from './components/Landing.vue'
import About from './components/About.vue'

export default {
    name: "App",
    components: {
      Landing,
      About
    }
}
</script>

<style>
  #app {
    height: 100vh;
    width: 100vw;
    color: rgb(215, 215, 215);
    text-align: center;
    background-color: black;
  }
</style>