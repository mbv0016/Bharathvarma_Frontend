<template>

  <!--Step 3 use the component-->
  <MyHeader storeName="Bharath Fashions"/> 
  <ClothingBox :products=products />
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import ClothingBox from './components/ClothingBox.vue'


export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    ClothingBox
  },
  data(){
    return {
      products: []
    }
  },
  methods:{
    //promoises
    async fetchcloths(){
      const res = await fetch('https://bharathvarma-backend-2.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.products = await this.fetchcloths();
  }

  // data() => this.data cloths
  // method => this.method => fetchcloths
  // life cycle hooks created() => call our method here

}
</script>


<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing:border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  background-image: url(https://static.vecteezy.com/system/resources/previews/026/579/366/non_2x/women-s-fashion-store-in-the-shopping-center-or-mall-clothes-store-with-mannequin-shopping-day-concept-by-ai-generated-free-photo.jpg);
    background-attachment:fixed ;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>