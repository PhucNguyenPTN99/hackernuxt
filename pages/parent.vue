<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Child :message="message" :value="value"/>
  </div>
</template>

<script>
import Child from '~/components/child.vue'

export default {
  components: {
    Child
  },
  data() {
    return {
      message: 'Xin chao tat ca moi nguoi',
      value: '1000 people'
    }
  }
}
</script>