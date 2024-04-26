<template>
   
    
    <div v-for="product of products" :key="product.id" >

     
       <SingleClothing :product=product />

    </div>

</template>
<script>
import SingleClothing from './SingleClothing.vue'

export default {
    name: 'ClothingBox',
    props:{
        products: Array
    },
    components:{
        SingleClothing
    }
    
}
</script>
<style scoped>

</style>