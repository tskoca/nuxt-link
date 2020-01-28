<template>
    <div class="container">
            <h3 class="title">Ürünü Düzenle</h3>
            <div class="input-container">
              <input type="text" v-model="productId">
              <button class="button--green" @click="changeProductId">Product Id Değiştir</button>
            </div>
            <div class="button-container">
            <nuxt-link to="/products" tag="a" class="button--green">Geri</nuxt-link>
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
 .title {
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }
 .container {
    min-height: 100vh;
    text-align: center;
    margin-top: 50px;
  }
 .button-container{
     margin-top:50px;
     border:1px solid #392;
     background-color:#dedede;
     padding:10px;
     box-shadow:2px 3px 8px rgba(0,0,0,.1);
     display: flex;
     justify-content: center;

 }.button--green{
     margin-left:5px;
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