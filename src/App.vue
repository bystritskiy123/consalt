<template>
  <div id="app">
    <HelloWorld />
    <Formablock />
    <Slider />
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import Formablock from './components/Formablock.vue'
  import Slider from './components/Slider.vue'

  export default {
    name: 'App',
    components: {
      HelloWorld,
      Formablock,
      Slider
    }
  }
</script>

<style lang="scss">

</style>