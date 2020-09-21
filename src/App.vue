<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  name: 'App',
  async mounted() {
    console.log('mounted start')
    await new Promise((resolve, reject) => {
      setTimeout(() => {
        console.log('i m mounted')
        resolve()
      }, 1000)
    })

    console.log('mounted end')
  }
})
</script>
