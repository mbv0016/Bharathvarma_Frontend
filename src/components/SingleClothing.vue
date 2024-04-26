<template>
    

    <div  :class="product.inventory > 80 ? 'green': 'blue' ">

                        <h2>{{product.name}}</h2>
                        <h4> {{product.category}}</h4>
                        <h4> {{product.price}}</h4>
                        <h4> {{product.color}}</h4>
                        <h4> {{product.brand}}</h4>
                        <h4> {{product.inventory}}</h4>
    </div>
</template>

<script>

export default{
    name: 'SingleClothing',
    props:{
        product: Array
    }
}
</script>

<style scoped>

.green{
    background-color: #225a2f;
}

h4{
    margin: 3px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.blue{
background-color:#9dd9d2  !important;

}


</style>