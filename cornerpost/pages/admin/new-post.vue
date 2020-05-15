<template>
  <post-form-comp @submit="savePost($event)" />
</template>

<script>
import PostFormComp from "~/components/admin/PostFormComp";
export default {
  components: {
    PostFormComp
  },
  methods: {
    savePost(post) {
      console.log(post);
    }
  }
};
</script>

<style scoped>
</style>
