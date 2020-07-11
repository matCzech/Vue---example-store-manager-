<template>
  <div id="app">
      <TheAddMultimeterPanel @add="multimeters.push($event)"/>
      <AboutMultimeterPanel 
      v-for="multimeter in multimeters"
      :name="multimeter.name"
      :model="multimeter.model"
      :state="multimeter.state"
      :aviailability="multimeter.aviailability"
      :key="multimeter.name"
      @remove="remove"/>
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
          model: '97',
          hp: 120,
          mp: 890
        },
        {
          name: 'UNI-T',
          model: 'UT 33C',
          hp: 690,
          mp: 80
        }
      ]
    }),
    methods: {
        remove(name){
            const index = this.multimeters.findIndex(v => v.name == name); 
            this.multimeters.splice(index, 1);
        }
    }
  }
</script>

<style>
  #app{
    padding:20px;
  }
</style>