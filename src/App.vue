<template>
  <div id="app">
    <header-box />
    <main-content />
  
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue';
import MainContent from './components/MainContent.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    MainContent,
    HeaderBox,
  },
  data(){
    return {
      dischi: []
    }
  },
  mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.dischi = response.data
    })
  },
}
</script>

<style lang="scss">
@import './style/common.scss';

</style>
