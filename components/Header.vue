<template>
  <header class="header">
    <ul class="navList">
      <li class="navItem">
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li class="navItem">
        <nuxt-link to="/users">Users</nuxt-link>
      </li>
      <li class="navItem">
        <nuxt-link to="/users/OTree">OTree Page</nuxt-link>
      </li>
      <li class="navItem">
        <nuxt-link to="/users/Kevin">Kevin Page</nuxt-link>
      </li>
    </ul>
  </header>
</template>
<style scoped>
.header {
  width: 100%;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.navList {
  width: 80%;
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
</style>