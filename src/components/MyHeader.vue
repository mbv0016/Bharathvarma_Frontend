<template>
<div>
    <h1> {{storeName}} </h1>
</div>
</template>

<script>

export default{ // Exporting Default Object
    name: 'MyHeader',
    props:{ 
        storeName:String
    }
}

</script>

<style scoped>

div{
    text-align: center;
}

</style>