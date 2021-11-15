<template>
  <section class="featured-posts">
    <PostPreview
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      :is-admin="isAdmin"
      :title="post.title"
      :thumbnail="post.thumbnail"
      :preview-text="post.previewText"
    />
  </section>
</template>
<script>
import PostPreview from "~/components/Posts/PostPreview.vue";

export default {
  name: 'PostList',
  components: {
    PostPreview,
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    },
    posts: {
      type: Array,
      default: () => [],
    },
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
