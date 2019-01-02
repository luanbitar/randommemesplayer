<template>
  <div id="app">
    <MainContainer name="container" />
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'

export default {
  name: 'app',
  components: {
    MainContainer
  }
}
</script>

<style>
  body {
    margin: 0;
    background-color: #1f1f1f;
  }
</style>
