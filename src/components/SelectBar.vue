<template>
    
    <div class="select-box d-flex justify-content-center pt-3">
        <select v-model="selected" class="form-select w-25" aria-label="Default select example">
            
           <option disabled value="">Please select one</option>
           <!-- <option v-for="(genre, index) in genres" :key="index" :value="genre.value">{{disc.genre}}</option>
         -->
        </select>

        <span>Selected: {{ selected }}</span>

    </div>
       
        
    
</template>

<script>



export default {
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