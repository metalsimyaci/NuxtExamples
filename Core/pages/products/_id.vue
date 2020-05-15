<template>
  <div class="container">
    <h2>Ürün Detayları</h2>
    <p>Ürün Anahtarı: {{$route.params.id}}</p>
    <nuxt-link tag="a" class="btn btn-primary" :to="'/products/edit/'+$route.params.id">Link</nuxt-link>
  </div>
</template>

<script>
export default {
  validate(arg) {
    console.log(arg);
    return /^\d+$/.test(arg.params.id);
  }
};
</script>

<style>
</style>
