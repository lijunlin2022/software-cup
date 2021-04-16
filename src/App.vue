<template>
  <div class="app">
    <main-navbar></main-navbar>
    <main>
      <router-view />
    </main>
  </div>
  <!-- <div id="nav"> -->
  <!-- <router-link to="/">Home</router-link> | -->
  <!-- <router-link to="/about">About</router-link> -->
  <!-- </div> -->
</template>

<script>
import MainNavbar from "@/components/content/mainNavbar/MainNavbar.vue";
export default {
  components: {
    MainNavbar,
  },
};
</script>

<style>
@import url(./assets/css/normalize.css);
@import url(./assets/css/style.css);
* {
  padding: 0;
  margin: 0;
}
.app > main {
  min-height: calc(100vh - 120px);
}
</style>
