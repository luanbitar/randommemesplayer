<template>
  <div class="container">
    <PlayItem v-for="audio in this.audios" :key="audio.title" v-bind:title="audio.title" v-bind:audio="audio.audioFile" v-bind:thumb="audio.thumb" />
  </div>
</template>

<script>
import PlayItem from './PlayItem.vue'
import audioFiles from '../assets/audios/'

export default {
  name: 'MainContainer',
  data: () => ({
    audios: audioFiles
  }),
  components: {
    PlayItem
  }
}
</script>

<style scoped>
  .container {
    --vertical-margin: 20px;
    display: grid;
    grid-template-columns: 33% 33% 33%; 
    grid-template-rows: auto;
    align-items: center;
    flex: 1;
    background-color: transparent;
    margin: 0 auto;
    min-height: 100vh;
    padding: var(--vertical-margin) 0;
    justify-content: center;
    max-width: 350px;
    box-sizing: border-box;
  }
</style>
