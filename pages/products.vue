<template>
<div>
<div class="input-container">
      <input type="text" v-model="productID">
      <button class="button--green" @click="showProduct"> Ürünü Göster</button>
    </div>
      <nuxt-child/>
</div>

</template>
<script>
  export default {
    data(){
      return {
        productID : this.$route.params.productId ? this.$router.params.productId :null
      }
    },
    methods : {
      showProduct(){
        this.$router.push("/products/" + this.productID)
      }
    }
  }
</script>
<style scoped>
.input-container{
    padding: 20px;
    border: 1px solid #688fb9;
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