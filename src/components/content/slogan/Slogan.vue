<template>
  <div class="slogan">
    <p>这是北京理工大学中国软件杯的参赛作品</p>
    <div class="btn-container">
      <button @click="goAbout">立即使用</button>
      <button>帮助文档</button>
      <button>代码仓库</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slogan",
  methods: {
    goAbout() {
      console.log(this.$router);
      this.$router.replace("/about");
    },
  },
};
</script>

<style scoped>
p {
  width: 90vw;
  margin: 100px auto;
  text-align: center;
  font-size: 32px;
}
.btn-container {
  text-align: center;
  margin-bottom: 200px;
}
.btn-container button {
  display: inline-block;
  width: 250px;
  height: 60px;
  margin: 10px;
  border: 1px solid #666;
  /* 消除边框的黑线 */
  outline: none;
  font-size: 16px;
  font-weight: bold;
  color: #fff;
  background: var(--assist-color);
}
.btn-container button:first-child {
  background-color: var(--main-color);
}
.btn-container button:hover {
  background-color: var(--main-color);
}
/* pc 端样式 */
@media screen and (min-width: 992px) {
  p {
    width: 770px;
    font-size: 50px;
  }
}
</style>
