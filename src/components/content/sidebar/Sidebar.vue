<template>
  <div class="sidebar">
    <div class="inner">
      <input type="checkbox" id="side" />
      <label for="side"></label>
      <ul>
        <li>
          <a href="javascript:void(0)">首页</a>
        </li>
        <li>
          <a href="javascript:void(0)">归档</a>
        </li>
        <li>
          <a href="javascript:void(0)">关于</a>
        </li>
        <li>
          <a href="javascript:void(0)">友情链接</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
};
</script>

<style scoped>
.sidebar {
  position: fixed;
}
.inner {
  position: absolute;
  top: 60px;
}
.inner input {
  /* 隐藏复选框 */
  display: none;
}
.inner label {
  position: relative;
  display: block;
  top: 0;
  left: 0;
  width: 40px;
  height: 40px;
  margin-bottom: 10px;
  background-color: #ff9200;
  transition: all 0.3s ease-out;
}
.inner ul {
  list-style: none;
  width: 40px;
  background-color: #fff;
  transition: all 0.3s ease-out;
}
.inner ul li {
  height: 70px;
  margin-bottom: 10px;
}
.inner ul li a {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  width: 100%;
  height: 100%;
  text-decoration: none;
  color: #fff;
  background-color: #333;
}
.inner ul li a:hover {
  background-color: #354962;
}
/* 选中之后的效果 */
.inner input:checked + label {
  width: 40px;
}
/* ~ 也是兄弟,可以找到隔了几代的兄弟 */
.inner input:checked ~ ul {
  width: 280px;
}
</style>
