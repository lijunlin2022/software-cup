<template>
  <div class="main-navbar">
    <p>中国软件杯</p>
    <navbar>
      <template v-slot:logo>
        <img src="../../../assets/img/logo.png" alt="" />
      </template>
      <ul>
        <li>
          <router-link to="/home">首页</router-link>
        </li>
        <li>
          <router-link to="/about">推流</router-link>
        </li>
        <li>
          <router-link to="/">占位置的</router-link>
        </li>
        <li>
          <router-link to="/">占位置的</router-link>
        </li>
        <li>
          <router-link to="/">占位置的</router-link>
        </li>
      </ul>
    </navbar>
  </div>
</template>

<script>
import Navbar from "../../common/navbar/Navbar.vue";
export default {
  components: {
    Navbar,
  },
};
</script>

<style scoped>
.main-navbar p {
  display: none;
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  height: 60px;
  line-height: 60px;
  text-align: center;

  background-color: var(--main-color);
}
@media screen and (min-width: 992px) {
  .main-navbar p {
    display: block;
  }
}
</style>
