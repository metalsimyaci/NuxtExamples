<template>
  <div class="container-fluid mt-5 d-flex flex-wrap justify-content-center align-items-center">
    <form style="width: 500px" @submit.prevent="onSubmit">
      <fieldset>
        <legend v-if="isUpdate">Köse Yazısı Düzenle</legend>
        <legend v-else>Yeni Köse Yazısı</legend>
        <div class="form-group">
          <label>Yazar Adı</label>
          <input
            type="text"
            class="form-control"
            placeholder="Yazarın adını giriniz.."
            v-model="post.author"
          />
        </div>
        <div class="form-group">
          <label>Baslık</label>
          <input
            type="text"
            class="form-control"
            placeholder="Yazının baslıgını giriniz.."
            v-model="post.title"
          />
        </div>
        <div class="form-group">
          <label>Alt Baslık</label>
          <input
            type="text"
            class="form-control"
            placeholder="Yazının alt baslıgını giriniz.."
            v-model="post.subTitle"
          />
        </div>
        <div class="form-group">
          <label for="exampleTextarea">Köse Yazısı</label>
          <textarea class="form-control" rows="5" v-model="post.text"></textarea>
        </div>
        <button @click="$router.push('/admin')" class="btn btn-danger">İptal</button>
        <button v-if="isUpdate" type="submit" class="btn btn-primary">Güncelle</button>
        <button v-else type="submit" class="btn btn-primary">Kaydet</button>
      </fieldset>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: {
    isUpdate: {
      type: Boolean,
      required: false,
      default: false
    },
    post: {
      type: Object,
      required: false,
      default: {
        title: null,
        subTitle: null,
        author: null,
        text: null
      }
    }
  },
  methods: {
    onSubmit() {
      this.$emit("submit", this.post);
    }
  }
};
</script>
