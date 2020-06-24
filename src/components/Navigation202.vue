<template>
  <div>
    <h1>component: {{ title }}</h1>

    <p><a href="/">home - hello world</a></p>
    <p><a href="/#/try">try</a></p>
  </div>
</template>

<script>
export default {
  name: 'Navigation202',
  data () {
    return {
      title: 'Navigation202'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1 {
    font-weight: normal;
  }
</style>
