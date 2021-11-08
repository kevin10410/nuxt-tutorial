<template>
  <div>
    <h1>Home Page</h1>
    <NuxtLink to="/users">Users page</NuxtLink>
    <NuxtLink to="/users/OTree">OTree page</NuxtLink>
    <NuxtLink to="/users/Kevin">Kevin page</NuxtLink>
  </div>
</template>
<script>
export default {
  layout: 'default',
};
</script>