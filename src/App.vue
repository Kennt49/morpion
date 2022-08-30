<template>
  <AccueilMorpion v-if="step == 1" @nextStep="nextStep"></AccueilMorpion>
  <ChoixMorpion v-if="step == 2" @nextStep="nextStep"></ChoixMorpion>
</template>

<script>
import AccueilMorpion from './components/AccueilMorpion.vue'
import ChoixMorpion from './components/ChoixMorpion.vue'
//import axios from 'axios';

export default {
  name: 'App',
  components: {
    AccueilMorpion,
    ChoixMorpion
  },
  data() {
    return {
      step: 1
    }
  },
  methods: {
    nextStep() {
      this.step++
    }
  }
}
</script>

<style>
/*#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
</style>
