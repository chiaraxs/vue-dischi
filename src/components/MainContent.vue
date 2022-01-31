<template>
    <div class="main d-flex flex-wrap pt-5">
        <loader-box/>
        <card-box v-for="(disc, index) in discs"
        :key="index"
        :disc="disc"
        class="card-box"
        />
    </div>
</template>

<script>
import CardBox from './CardBox.vue'


export default {
    components: {
    CardBox,
    },
    props:{
        discs: Array,
    }
 
    
}
</script>


<style lang="scss" scoped>

.main{
    padding: 150px 400px;
    height: 100vh;
    background-color: #1E2D3B;


    .card-box{
        margin: 10px;
        width: 200px;
        height: 350px;
        background-color: #2E3A46;

        
    }
}


</style>