<template>
  <div class="post-page">
    <PostList />
  </div>
</template>
<script>
import PostList from "~/components/Posts/PostList.vue";

export default {
  name: 'Posts',
  components: {
    PostList,
  },
}
</script>
