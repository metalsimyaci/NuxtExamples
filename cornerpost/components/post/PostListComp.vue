<template>
  <div class="container-fluid mt-5 d-flex flex-wrap justify-content-center align-items-center">
    <post-comp :post="post" v-for="post in posts" :key="post.id" :is-admin="isAdmin" />
  </div>
</template>
<script>
import PostComp from "~/components/post/PostComp";
export default {
  components: {
    PostComp
  },
  props: {
    isAdmin: {
      type: Boolean,
      required: false,
      default: false
    },
    posts: {
      required: true,
      type: Array
    }
  }
};
</script>
