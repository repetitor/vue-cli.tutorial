<template>
  <div>
    <h1>component: {{ title }}</h1>

    <navigation/>

    <p>message: {{ message }}</p>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'AxiosPostLogin',

  data () {
    return {
      title: 'AxiosPostLogin',
      message: 'default'
    }
  },

  components: {
    Navigation: () => import('@/components/axios/AxiosNavigation')
  },

  mounted () {
    const JS_BACKEND_API = 'http://localhost:91/api'
    const JS_USER_NAME = 'vue cli name'
    const JS_USER_EMAIL = 'vuecli$email.rr3'
    const JS_USER_PASSWORD = 'password'

    axios.post(
      JS_BACKEND_API + '/login',
      {
        'name': JS_USER_NAME,
        'email': JS_USER_EMAIL,
        'password': JS_USER_PASSWORD
      },
      {
        'Content-Type': 'application/json',
        'Accept': 'application/json'
      }
    )
      .then(response => {
        console.log(response.data)
        this.message = response.data.access_token
      })
  }
}
</script>
