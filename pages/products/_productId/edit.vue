<template>
    <div class="container">
            <div class="input-container">
              <input type="text" v-model="productId">
              <button class="button--green" @click="changeProductId">Product Id Değiştir</button>
            </div>
    </div>
</template>

<script>
   export default{
       data(){
          return {
              productId:this.$route.params.productId
              }
          
       },
       methods:{
           changeProductId(){
               this.$router.push('/products/'+this.productId)
           }
       }
 }
</script>

<style>
.container {
    min-height: 100vh;
    text-align: center;
    margin-top: 50px;
  }
 .input-container{
    padding: 20px;
    border: 1px solid #688fb9;
    margin-top: 50px;
    background-color: #35495e;
    box-shadow: 2px 3px 8px rgba(0,0,0,.1);

  }

  input{
    border: none;
    outline: none;
    height: 30px;
    font-size: 18px;
    color: #35495e;
  }
</style>