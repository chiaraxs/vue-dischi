<template>
    
    <div class="select-box d-flex justify-content-center pt-3">
        <select v-model="selected" @change="$emit('selectedGenre', selected)" class="form-select w-25" aria-label="Default select example">
            
           <option disabled value="">Select genre</option>
           <option v-for="(genre, index) in values" :key="index" :value="genre">{{genre}}</option>
           
        </select>

        

    </div>
       
        
    
</template>

<script>



export default {
    props: {
        values: Array
    },
    data(){
        return{
            selected: ''
        }
        
    }
    
}
</script>


<style lang="scss" scoped>
.select-box{
    background-color: #1E2D3B;
}

</style>