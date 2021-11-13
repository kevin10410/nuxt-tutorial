<template>
  <form @submit.prevent="onSubmit">
    <AppControlInput
      v-model="editedPost.author"
    >
      Author Name
    </AppControlInput>
    <AppControlInput
      v-model="editedPost.title"
    >
      Title
    </AppControlInput>
    <AppControlInput
      v-model="editedPost.thumbnailLink"
    >
      Thumbnail Link
    </AppControlInput>
    <AppControlInput
      v-model="editedPost.content"
      control-type="textarea"
    >
      Content
    </AppControlInput>
    <AppButton type="submit">Save</AppButton>
    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel"
    >
      Cancel
    </AppButton>
  </form>
</template>
<script>
import AppButton from '~/components/UI/AppButton.vue';
import AppControlInput from '~/components/UI/AppControlInput.vue';

export default {
  name: 'AdminPostForm',
  components: {
    AppButton,
    AppControlInput,
  },
  props: {
    post: {
      type: Object,
      required: false,
      default: () => ({
        title: '',
        author: '',
        content: '',
        thumbnailLink: '',
      }),
    },
  },
  data() {
    return {
      editedPost: {
        title: '',
        author: '',
        content: '',
        thumbnailLink: '',
      },
    };
  },
  mounted() {
    if (this.post) {
      this.editedPost = { ...this.post };
    }
  },
  methods: {
    onSubmit() {

    },
    onCancel() {
      this.$router.push('/admin');
    },
  },
};
</script>
