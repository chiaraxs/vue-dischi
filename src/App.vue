<template>
  <div id="app">
    <header-box />
    <loader />
    <main-content :discs = "discs" />
    
  
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
      discs: []
    }
  },
  mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.discs = response.data.response
    })
  },
}
</script>

<style lang="scss">
@import './style/common.scss';

</style>
