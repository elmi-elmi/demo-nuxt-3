<template>
  <form @submit.prevent=""onSave>
    <AppControlInput v-model="editedPost.author">Author Name</AppControlInput>

    <AppControlInput v-model="editedPost.title">Title</AppControlInput>

    <AppControlInput v-model="editedPost.thumbnail">Thumbnail Link</AppControlInput>

    <AppControlInput
      control-type="textarea"
      v-model="editedPost.content">Content
    </AppControlInput>

    <AppButton type="submit">Save</AppButton>

    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel">Cancel
    </AppButton>
  </form>
</template>

<script>
import AppButton from "@/components/UI/AppButton";
import AppControlInput from "@/components/UI/AppControlInput";
export default {
  name: "AdminPostForm",
  props:{
    post:{
      type:Object,
      required:true
    }
  },
  components:{
    AppControlInput,AppButton
  },
  data() {
    return {
      editedPost: this.post?{...this.post}:{
        author: '',
        title: '',
        thumbnail: '',
        content: ''
      }
    }
  },
  methods: {
    onSave() {
      //save the post
    },
    onCancel() {
      //Navigate back
      this.$router.push('/admin')
    }
  }
}
</script>

<style scoped>

</style>
