<template>
  <div class="container">
    <h1>Ürünler</h1>
    <a href="/categories">Kateoriler</a>
    <nuxt-link to="/categories" tag="a" class="btn btn-primary">Kateoriler router</nuxt-link>
    <div class="input-container">
      <input type="text" v-model="productId" />
      <button @click="showProductDetail">Ürün detayını getir</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      productId:null
    }
  },
  methods:{
    showProductDetail(){
      this.$router.push("/products/"+this.productId);
    }
  }
}
</script>

<style>
</style>
