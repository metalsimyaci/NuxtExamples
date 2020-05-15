<template>
  <div>
    <post-list-comp :posts="fetchedPosts" />
    <about-comp />
  </div>
</template>

<script>
import PostListComp from "@/components/post/PostListComp";
import AboutComp from "@/components/home/AboutComp";
export default {
  components: {
    PostListComp,
    AboutComp
  },
  // data() {
  //   return {
  //     fetchedPosts: []
  //   };
  // },
  created() {
    this.$store.dispatch("setPosts", this.fetchedPosts);
  },
  fetch(context) {
    
    
      return new Promise(null, {
        fetchedPosts: [
          {
            id: 1,
            title: "Title1",
            subTitle: "SubTitle1",
            text: "Lorem inpus Dolar sit amen",
            author: "bla1"
          },
          {
            id: 2,
            title: "Title2",
            subTitle: "SubTitle2",
            text: "Lorem inpus Dolar sit amen",
            author: "bla2"
          },
          {
            id: 3,
            title: "Title3",
            subTitle: "SubTitle3",
            text: "Lorem inpus Dolar sit amen",
            author: "bla3"
          },
          {
            id: 4,
            title: "Title4",
            subTitle: "SubTitle4",
            text: "Lorem inpus Dolar sit amen",
            author: "bla4"
          },
          {
            id: 5,
            title: "Title5",
            subTitle: "SubTitle5",
            text: "Lorem inpus Dolar sit amen",
            author: "bla5"
          }
        ]
      });
    }, 2000);
  }
};
</script>

<style scoped></style>
