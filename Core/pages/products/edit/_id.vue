<template>
  <div class="container">
    <h2>Ürün Düzenleme Ekranı</h2>
    <div class="container-fluid">
      <input type="text" v-model="productId" />
    </div>
    <p>
      <input type="text" />
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productId: null
    };
  },
  mounted(){
    this.productId=this.$route.params.id;
  }
};
</script>

<style>
</style>
