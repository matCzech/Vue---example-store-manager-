<template>
  <div id="app">
      <TheAddMultimeterPanel/>
      <AboutMultimeterPanel v-for="multimeter in multimeters"/>
  </div>
</template>

<script>
  import TheAddMultimeterPanel from './components/TheAddMultimeterPanel.vue';
  import AboutMultimeterPanel from './components/AboutMultimeterPanel.vue';
  export default {
    name: 'app',
    components: {
        TheAddMultimeterPanel,
        AboutMultimeterPanel
    },
    data: () => ({
      multimeters:[
        {
          name: 'Fluke',
          pseudo: '97',
          hp: 120,
          mp: 890
        },
        {
          name: 'UNI-T',
          pseudo: 'UT 33C',
          hp: 690,
          mp: 80
        }
      ]
    })
  }
</script>

<style>
  #app{
    padding:20px;
  }
</style>