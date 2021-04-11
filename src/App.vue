<template>
  <!-- <div id="nav"> -->
  <!-- <router-link to="/">Home</router-link> | -->
  <!-- <router-link to="/about">About</router-link> -->
  <!-- </div> -->
  <navbar></navbar>
  <router-view />
</template>

<script>
import Navbar from "@/components/navbar/Navbar.vue";

export default {
  components: {
    Navbar,
  },
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
}
body {
  min-height: 100vh;
  background: url(./assets/img/bg2.jpg) no-repeat;
  background-size: cover;
}
@media screen and (max-width: 768px) {
  body {
    background-image: linear-gradient(#000, #0f3a58);
  }
}
</style>
