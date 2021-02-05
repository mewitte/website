<template>
  <div id="home" v-bind:style="{ backgroundImage: 'url(' + backgroundImage + ')' }">
    <h1>Hello there!</h1>
    I am Melvin Witte, a software engineer. I am passionate about clean, pragmatic code.
    <div id="more">
      <span>Learn more about me</span>
      <b-icon icon="caret-down"></b-icon>
    </div>
  </div>
</template>

<script>
export default {
  name: "Landing",
  props: [ "backgroundImage" ]
}
</script>

<style>
  #home {
    height: 100vh;
    width: 100vw;
    position: relative;
    display: table-cell;
    vertical-align: middle;
  }

  #more {
    width: 100vw;
    position: absolute;
    bottom: 0;
    margin-bottom: 15px;
  }
</style>