<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news!</h1>
    </section>
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
  </div>
</template>
<script>
import PostPreviewVue from "~/components/Posts/PostPreview.vue";

export default {
  components: {
    PostPreviewVue,
  },
  layout: 'default',
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
};
</script>
<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>