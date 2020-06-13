<template>
  <div id="app">
    <HelloWorld />
    <Formablock />
    <Slider />
    <Textblock />
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import Formablock from './components/Formablock.vue'
  import Slider from './components/Slider.vue'
  import Textblock from './components/Textblock.vue'

  export default {
    name: 'App',
    components: {
      HelloWorld,
      Formablock,
      Slider,
      Textblock
    }
  }
</script>

<style lang="scss">

</style>