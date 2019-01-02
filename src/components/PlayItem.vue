<template>
  <div class="line" v-on:click="play">
    <img v-bind:src="thumb" class="thumbnail">
    <p class="title">{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: 'PlayItem',
  props: ['title', 'audio', 'thumb'],
  methods: {
    play: function () {
      this.audio.play()
    }
  }
}
</script>

<style scoped>
  .line {
    background-color: transparent;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-self: center;
    text-align: center;
    align-items: center;
    outline: none;
    padding-bottom: 10px;
  }
  .title {
    flex: 1;
    height: 100%;
    color: #b1b1b1;
    font-family: monospace;
    font-size: 1rem;
    font-weight: 700;
    border: 0;
    background: transparent;
    margin: 0;
    padding-top: 5px;
  }
</style>
