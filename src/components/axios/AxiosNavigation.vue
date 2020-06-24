<template>
  <div>
    <h1>component: {{ title }}</h1>

    <p><a href="/#/axios/get">axios/get</a></p>
    <p><a href="/#/axios/post-register">axios/post-register</a></p>
    <p><a href="/#/axios/post-login">axios/post-login</a></p>
  </div>
</template>

<script>
export default {
  name: 'AxiosNavigation',
  data () {
    return {
      title: 'AxiosNavigation'
    }
  }
}
</script>
