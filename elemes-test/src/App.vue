<template>
  <landingPage/>
</template>

<script>
import landingPage from './components/landingPage/landingPage.vue'

export default {
  name: 'App',
  components: {
    landingPage
  }
}
</script>

<style>
#app {
  font-family: 'Rubik', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
