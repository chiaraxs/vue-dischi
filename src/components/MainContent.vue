<template>
    <div class="main">
        <card-box v-for="(disc, index) in discs"
        :key="index"
        :disc="disc"
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

main{
    display: flex;
    background-color: #1E2D3B;
}


</style>