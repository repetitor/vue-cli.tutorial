<template>
  <div>
    <h1>{{ title }}</h1>

    <navigation/>
  </div>
</template>

<script>
export default {
  name: 'Axios',
  data () {
    return {
      title: 'component: Axios'
    }
  },

  components: {
    Navigation: () => import('@/components/axios/AxiosNavigation')
  }
}
</script>
