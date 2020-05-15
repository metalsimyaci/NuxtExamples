<template>
  <post-form-comp :is-update="true" :post="fetchedPost" />
</template>

<script>
import PostFormComp from "~/components/admin/PostFormComp";
export default {
  components: {
    PostFormComp
  },
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        fetchedPost: {
          id: 1,
          title: "Title1",
          subTitle: "Adolphus85",
          text:
            "Officiis eum consequuntur sit expedita. Magnam sed sed sit ipsam ea. Sit occaecati cupiditate optio.",
          author: "Matilda Ziemann"
        }
      });
    }, 1500);
  }
};
</script>

<style scoped>
</style>
