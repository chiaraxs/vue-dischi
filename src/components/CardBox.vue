<template>
    <div class="container-card">
        
        <div class="dischi">
            <img :src="disc.poster">
            <h4>{{disc.title}}</h4>
            <h6>{{disc.author}}</h6>
            <h6>{{disc.year}}</h6>
        </div>
    
    </div>
</template>



<script>
export default {
    props: {
        disc: Object
    }
 
    
}
</script>


<style lang="scss" scoped>


</style>