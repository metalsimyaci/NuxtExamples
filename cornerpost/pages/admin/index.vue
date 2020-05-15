<template>
  <div>
    <div class="container d-flex justify-content-center align-items-center">
      <button @click="$router.push('/admin/new-post')" class="btn btn-dark">Yeni Bir Yazı Ekle</button>
    </div>
    <post-list-comp :posts="fetchedPosts" :is-admin="true" />
  </div>
</template>

<script>
import PostListComp from "@/components/post/PostListComp";
export default {
  layout: "admin",
  components: {
    PostListComp
  },
  data() {
    return {
      fetchedPosts: []
    };
  },
  asyncData(context) {
    return new Promise(resolve => {
      resolve({
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
    });
  }
};
</script>

<style scoped></style>
