<template>
  <div>
    <Header/>
    <h1>The users view</h1>
    <NuxtChild />
  </div>
</template>
<script>
import Header from '~/components/Header.vue';

export default {
  components: {
    Header,
  },
  layout: 'users',
};
</script>
