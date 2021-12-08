<template>
  <div>
    <section class="post-list">
      <PostPreview :is-admin="isAdmin" id="1" title="Title 1" preview-text="preview text 1"
                   thumbnail='_nuxt/assets/images/coding_languages.png'/>
      <PostPreview :is-admin="isAdmin" id="2" title="Title 2" preview-text="preview text 2"
                   thumbnail='_nuxt/assets/images/coding2.jpeg'/>
    </section>
  </div>
</template>

<script>
import PostPreview from "~/components/posts/PostPreview";

export default {
  name: "PostList",
  props: {
    isAdmin: {
      type: Boolean,
      required: false
    },
  },
  components: {
    PostPreview
  }
}
</script>

<style scoped>

.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

</style>
