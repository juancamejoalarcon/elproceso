<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Step v-bind:step="this.currentStep"/>
  </div>
</template>

<script>
import Step from './components/Step.vue'

export default {
  name: 'App',
  components: {
    Step
  },
  data() {
    return {
      currentStep: {},
      anonima: [ true, false, true],
      unipersonal: [ true, false, true],
      steps: [
        {
          id: 0,
          question: 'Más de 50.000'
        },
        {
          id: 1,
          question: 'Nacionalidad española'
        },
        {
          id: 2,
          question: 'Más de 100 trabajadores'
        }
      ]
    }
  },
  methods: {
  },
  created() {
    this.currentStep = this.steps[0];
    console.log(this.steps);
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
