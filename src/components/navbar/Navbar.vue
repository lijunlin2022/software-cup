<template>
  <header>
    <nav>
      <ul>
        <li>
          <router-link to="/home">
            <div class="box">
              <div class="front">首页</div>
              <div class="bottom">HOME</div>
            </div>
          </router-link>
        </li>
        <li>
          <router-link to="/about">
            <div class="box">
              <div class="front">推流</div>
              <div class="bottom">FLOW</div>
            </div>
          </router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
header {
  height: 10vh;
}
nav ul {
  position: fixed;
  display: flex;
  display: -webkit-flex;
  justify-content: space-around;
  width: 100vw;
  height: 10vh;
}
nav ul li {
  list-style: none;
  width: 100%;
  height: 100%;
}
.box {
  position: relative;
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transition: all 0.4s;
}
.box:hover {
  transform: rotateX(90deg);
}
.front,
.bottom {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  text-align: center;
  line-height: 10vh;
  color: #fff;
  font-size: 1.5em;
  font-family: Oswald, "Microsoft Yahei", Arial, Helvetica, sans-serif;
  box-shadow: 0 0 2px #ccc;
}
.front {
  background-image: linear-gradient(#000, #101324);
  z-index: 1;
  transform: translateZ(5vh);
}
.bottom {
  background-image: linear-gradient(#d15b3d, #101324);
  /* 如果有移动或者其他样式, 需要先写移动 */
  transform: translateY(5vh) rotateX(-90deg);
}
</style>
