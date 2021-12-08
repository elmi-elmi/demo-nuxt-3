<template>
<div class="admin-post-page">
  <section class="update-form">
<AdminPostForm :post="loadedPost"/>
  </section>
</div>
</template>

<script>
import AdminPostForm from "@/components/Admin/AdminPostForm";
export default {
  name: "index",
  components:{AdminPostForm},
  data(){
    return{
      loadedPost:{
        author:'Shahrokh',
        title:'title 1',
        content:'content 1',
        thumbnail:'_nuxt/assets/images/coding_languages.png'
      }
    }
  }
}
</script>

<style scoped>

</style>
