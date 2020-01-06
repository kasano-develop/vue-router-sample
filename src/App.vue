<template>
  <div style="width:700px; margin: auto; padding-top:50px;">
    <nav>
      <!-- <a href="/">Home</a>
      <a href="/users">Users</a> -->
      <router-link
        to="/"
        class="link"
        active-class="link--active"
        exact
        >Home</router-link>
      <router-link
      to="/users"
      class="link"
      active-class="link--active"
      exact
      >Users
      </router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
// import Home from './views/Home.vue';
// export default {
//   components: {
//     Home
//   }
// }
</script>

<style scoped>
.link {
  margin-right: 10px;
}
.link--active {
  font-size: 20px;
}

</style>