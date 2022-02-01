<template>
  <div id="app">
    
    <header-box /> 
    <select-bar :values="['All','Pop', 'Rock', 'Jazz', 'Metal']" @selectedGenre="filterResults"/> 
    
    <main-content v-if="load === true" :discs = "filteredListGenre" />
    <loader v-else/>
    
  
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue';
import MainContent from './components/MainContent.vue';
import Loader from './components/Loader.vue';
import SelectBar from './components/SelectBar.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    MainContent,
    HeaderBox,
    Loader,
    SelectBar,
  },
  data(){
    return {
      discs: [],
      load: false,
      filteredListGenre: [],
    }
  },
  mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.load = true;
      this.discs = response.data.response;
      this.filteredListGenre = response.data.response;
    })
  },
  methods: {
    filterResults(keyword){
      this.filteredListGenre = this.discs.filter((disc) => {
        return disc.genre.toLowerCase() === keyword.toLowerCase() || keyword.toLowerCase() === 'all';
      });
    }
  }
}
</script>

<style lang="scss">
@import './style/common.scss';

</style>
