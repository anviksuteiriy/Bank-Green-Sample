<template>
  <div id="app">
    <SampleUI msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import SampleUI from './components/SampleUI.vue'

export default {
  name: 'App',
  components: {
    SampleUI
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
.slick-list {
  max-height: 300px;
  border-top-left-radius: 1rem;
  border-top-right-radius: 1rem;
}
.slick-dots {
  bottom: 8px;
}
.slick-dots li.slick-active button:before {
  color: white;
}
.slick-dots li button:before {
  color: white;
}
</style>
