<template>
  <div id="app">
    <button @click="randomize">randomize</button>
    <input type="checkbox" v-model="functional">
    <div v-if="functional">
      <functional v-for="i in 10000" :rng="rng()" :key="i" />
    </div>
    <div v-else>
      <normal v-for="i in 10000" :rng="rng()" :key="i" />
    </div>

  </div>
</template>

<script>
import Functional from './components/Functional.vue'
import Normal from './components/Normal.vue'

export default {
  name: 'app',
  components: {
    Functional,
    Normal
  },
  data() {
    return {
      functional: true,
      reload: 0
    }
  },
  computed: {
    rng() {
      return () => Math.random() + (this.reload * 0)
    }
  },
  methods: {
    randomize() {
      this.reload += 1
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
