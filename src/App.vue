<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
    <hr />
    <p>template - p bottom</p>
    <p><a href="/">home - hello world</a></p>
    <p><a href="/#/try">try</a></p>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
