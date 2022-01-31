<template>
    <div class="container-card">
        
        <div class="discs ">
            <img :src="disc.poster">
            <h5>{{disc.title}}</h5>
            <p>{{disc.author}}
            <br>
            {{disc.year}}</p>
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

.discs{
    
    color: white;
    text-align: center;

    img{
        width: 200px;
        padding: 10px;
    

    }

    h5{
        text-transform: uppercase;
        font-weight: bolder;
        font-size: 18px;
        margin-top: 5px;
    }

    p{
        color: grey;
        margin-top: 20px;
    }
}

</style>