<template>
  <div>
    <h1>{{ title }}</h1>

    <navigation/>

    <p>message: {{ message }}</p>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'AxiosGet',

  data () {
    return {
      title: 'component: AxiosGet',
      message: 'default'
    }
  },

  components: {
    Navigation: () => import('@/components/axios/AxiosNavigation')
  },

  mounted () {
    const JS_BACKEND_API = 'http://localhost:91/api'

    axios.get(
      JS_BACKEND_API + '/get-public-data',
      {
        'Content-Type': 'application/json',
        'Accept': 'application/json'
      }
    )
      .then(response => {
        console.log(response.data)
        this.message = response.data
      })
  }
}
</script>
