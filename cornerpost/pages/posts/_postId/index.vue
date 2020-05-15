<template>
  <post-detail-comp :post="fetchedPost" />
</template>

<script>
import PostDetailComp from "@/components/post/PostDefailComp";
export default {
  components: {
    PostDetailComp
  },
  async asyncData(context) {
    // setTimeout(() => {
    return new Promise((resolve, reject) => {
      resolve({
        fetchedPost: {
          id: context.params.postId,
          title: "Title1",
          subTitle: "SubTitle1",
          text: "Lorem inpus Dolar sit amen",
          author: "bla1  " + context.params.postId
        }
      });
    }).then(data => {
      console.log(data);
      return data;
    });
    //   callback(null, {
    //     fetchedPost: {
    //       id: context.params.postId,
    //       title: "Title1",
    //       subTitle: "SubTitle1",
    //       text: "Lorem inpus Dolar sit amen",
    //       author: "bla1  " + context.params.postId
    //     }
    //   });
    // }, 1500);
  }
};
</script>

<style scoped>
</style>
