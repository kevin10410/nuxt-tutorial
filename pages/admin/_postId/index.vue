<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm
        :post="loadedPost"
      />
    </section>
  </div>
</template>
<script>
import AdminPostForm from '~/components/Admin/AdminPostForm.vue';

export default {
  name: 'EditPost',
  components: {
    AdminPostForm,
  },
  layout: 'admin',
  data() {
    return {
      loadedPost: {
        title: "OTree's awesome Post",
        author: 'OTree',
        content: 'Post content...',
        thumbnail: 'https://images.unsplash.com/photo-1607706189992-eae578626c86?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80',
      },
    };
  },
}
</script>
<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}

@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
