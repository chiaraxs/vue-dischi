<template>
  <div id="app">
    <header-box />
    <main-content v-if="load === true" :discs = "discs" />
    <loader v-else/>
    
  
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue';
import MainContent from './components/MainContent.vue';
import Loader from './components/Loader.vue'
import axios from 'axios';

export default {
  name: 'App',
  components: {
    MainContent,
    HeaderBox,
    Loader,
  },
  data(){
    return {
      discs: [],
      load: false,
    }
  },
  mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.load = true;
      this.discs = response.data.response;
    })
  },
}
</script>

<style lang="scss">
@import './style/common.scss';

</style>
