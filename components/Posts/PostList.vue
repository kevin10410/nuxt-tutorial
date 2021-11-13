<template>
  <section class="featured-posts">
    <PostPreviewVue
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      :title="post.title"
      :thumbnail="post.thumbnail"
      :preview-text="post.previewText"
    />
  </section>
</template>
<script>
import PostPreviewVue from "~/components/Posts/PostPreview.vue";

export default {
  name: 'PostList',
  components: {
    PostPreviewVue,
  },
  data() {
    return {
      posts: [
        {
          id: 'OTree',
          title: 'OTree Post Title',
          previewText: 'Preview Text',
          thumbnail: 'https://images.unsplash.com/photo-1607706189992-eae578626c86?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80',
        },
        {
          id: 'Kevin',
          title: 'Kevin Post Title',
          previewText: 'Preview Text',
          thumbnail: 'https://images.unsplash.com/photo-1607706189992-eae578626c86?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80',
        },
      ],
    };
  },
}
</script>
<style scoped>
.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
