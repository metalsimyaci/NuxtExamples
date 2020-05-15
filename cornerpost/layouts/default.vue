<template>
  <div>
    <header-comp />
    <banner-comp />
    <nuxt />
  </div>
</template>
<script>
import HeaderComp from "@/components/common/HeaderComp";
import BannerComp from "@/components/common/BannerComp";
export default {
  components: {
    HeaderComp,
    BannerComp
  }
};
</script>
