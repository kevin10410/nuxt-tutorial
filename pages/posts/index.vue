<template>
  <div class="post-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>
<script>
import PostList from "~/components/Posts/PostList.vue";

export default {
  name: 'Posts',
  components: {
    PostList,
  },
  data() {
    return {
      loadedPosts: [
        {
          author: 'OTree',
          title: 'OTree Post Title',
          previewText: 'Preview Text',
          thumbnail: 'https://images.unsplash.com/photo-1607706189992-eae578626c86?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80',
        },
        {
          author: 'Kevin',
          title: 'Kevin Post Title',
          previewText: 'Preview Text',
          thumbnail: 'https://images.unsplash.com/photo-1607706189992-eae578626c86?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80',
        },
      ],
    };
  },
}
</script>
