<template>
  <div id="app">
    <HelloWorld />
    <Formablock />
    <Slider />
    <Textblock />
    <Calculator />
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import Formablock from './components/Formablock.vue'
  import Slider from './components/Slider.vue'
  import Textblock from './components/Textblock.vue'
  import Calculator from './components/Calculator.vue'

  export default {
    name: 'App',
    components: {
      HelloWorld,
      Formablock,
      Slider,
      Textblock,
      Calculator
    }
  }
</script>

<style lang="scss">

</style>