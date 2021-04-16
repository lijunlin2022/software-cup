<template>
  <header>
    <div class="logo">
      <slot name="logo"></slot>
    </div>
    <nav>
      <div>
        <input type="checkbox" id="nav" />
        <label for="nav"></label>
        <slot></slot>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
header {
  display: flex;
}
.logo {
  display: none;
  position: relative;
  width: 60px;
  height: 60px;
}
.logo > img {
  position: absolute;
  display: block;
  width: 40px;
  height: 40px;
  top: calc(50% - 20px);
  left: 10px;
}
nav {
  width: 100vw;
  height: 60px;
  position: relative;
  background-color: var(--main-color);
}
nav input {
  /* 隐藏复选框 */
  display: none;
}
/* 使用 label 模拟手机端展开和关闭 navbar 的按钮 */
nav label {
  position: absolute;
  right: 30px;
  width: 30px;
  height: 30px;
  /* 垂直居中 */
  top: calc(50% - 15px);
  border-radius: 3px;
  background-color: #fff;
}
/* 利用伪元素画出两条线 */
nav label::before,
nav label::after {
  content: "";
  position: absolute;
  width: 20px;
  height: 2px;
  /* 水平居中 */
  left: 5px;
  background-color: #999;
  /* 复选框被取消选中后的动画 */
  transition: transform 0.3s ease-out, top 0.3s ease-out;
}
nav label::before {
  top: calc(50% - 4px);
}
nav label::after {
  top: calc(50% + 4px);
}
/* 定义复选框被选中时两天线条的位置和动画 */
nav input:checked + label::before {
  top: calc(50% - 2px);
  transform: rotate(-45deg);
  transition: top 0.3s ease-out, transform 0.3s ease-out;
}
nav input:checked + label::after {
  top: calc(50% - 2px);
  transform: rotate(45deg);
  transition: top 0.3s ease-out, transform 0.3s ease-out;
}
/* 移动端的导航栏样式 */
nav ul {
  position: relative;
  top: 60px;
  width: 100%;
  margin: 0;
  padding: 0;
  /* 未选中时默认不现实 */
  opacity: 0;
  transform: scaleY(0);
  /* 让缩放点在顶端中心 */
  transform-origin: 50% 0;
  transition: all 0.3s ease-out;
}
nav ul li {
  width: 100%;
  height: 59px;
  border-bottom: 1px solid #e6e6e6;
  background-color: #fff;
  text-align: center;
  list-style: none;
}
nav ul li:hover {
  border-bottom: 2px solid var(--main-color);
}
nav ul li a {
  display: block;
  width: 100%;
  height: 100%;
  line-height: 60px;
  font-size: 16px;
  text-align: center;
  text-decoration: none;
  color: #666;
}
/* 选中后会有一个下拉的动画 */
nav input:checked ~ ul {
  opacity: 1;
  transform: scaleY(1);
}

/* pc 端样式 */
@media screen and (min-width: 992px) {
  .logo {
    display: block;
  }
  nav {
    background-color: #fff;
  }
  nav label {
    display: none;
  }
  nav ul {
    /* 回归静态定位 */
    position: static;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    width: 1200px;
    margin: 0 auto;
    height: 100%;

    /* 元素一直存在, 不会隐藏 */
    opacity: 1;
    transform: scaleY(1);
  }
  nav ul li {
    list-style: none;
  }
}
</style>
