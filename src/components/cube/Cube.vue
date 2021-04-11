<template>
  <main>
    <div class="cube">
      <div class="img1"></div>
      <div class="img2"></div>
      <div class="img3"></div>
      <div class="img4"></div>
      <div class="img5"></div>
      <div class="img6"></div>
    </div>
  </main>
</template>

<script>
export default {
  name: "Cube",
};
</script>

<style scoped>
main {
  width: 70vw;
  margin: 10vh auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
.cube {
  position: relative;
  width: 10vw;
  height: 10vw;
  transform-style: preserve-3d;
  animation: rotate-cube 10s ease-in-out infinite;
}
.cube > div {
  position: absolute;
  width: 10vw;
  height: 10vw;
  background-size: cover;
  opacity: 0.95;
  border-radius: 5px;
  box-shadow: inset 0 0 4px 2px rgba(106, 106, 106, 0.4);
  z-index: -1;
}
/* 前 */
.cube .img1 {
  background-image: url(../../assets/img/1.jpg);
  transform: rotateY(0deg) translateZ(5vw);
}
/* 右 */
.cube .img2 {
  background-image: url(../../assets/img/2.jpg);
  transform: rotateY(90deg) translateZ(5vw);
}
/* 左 */
.cube .img3 {
  background-image: url(../../assets/img/3.jpg);
  transform: rotateY(-90deg) translateZ(5vw);
}
/* 下 */
.cube .img4 {
  background-image: url(../../assets/img/4.jpg);
  transform: rotateX(90deg) translateZ(5vw);
}
/* 上 */
.cube .img5 {
  background-image: url(../../assets/img/5.jpg);
  transform: rotateX(-90deg) translateZ(5vw);
}
/* 后 */
.cube .img6 {
  background-image: url(../../assets/img/6.jpg);
  transform: rotateY(180deg) translateZ(5vw);
}

@keyframes rotate-cube {
  0% {
    /* 前 */
    transform: rotateX(0deg) rotateY(0deg);
  }
  16% {
    /* 右 */
    transform: rotateY(-90deg);
  }
  32% {
    /* 上 */
    transform: rotateX(-90deg);
  }
  48% {
    /* 左 */
    transform: rotateY(90deg);
  }
  64% {
    /* 下 */
    transform: rotateX(90deg);
  }
  80% {
    /* 后 */
    transform: rotateY(180deg);
  }
}

@media screen and (max-width: 768px) {
  .cube {
    width: 20vw;
    height: 20vw;
  }
  .cube > div {
    width: 20vw;
    height: 20vw;
  }
  .cube .img1 {
    transform: rotateY(0deg) translateZ(10vw);
  }
  .cube .img2 {
    transform: rotateY(90deg) translateZ(10vw);
  }
  .cube .img3 {
    transform: rotateY(-90deg) translateZ(10vw);
  }
  .cube .img4 {
    transform: rotateX(90deg) translateZ(10vw);
  }
  .cube .img5 {
    transform: rotateX(-90deg) translateZ(10vw);
  }
  .cube .img6 {
    transform: rotateX(180deg) translateZ(10vw);
  }
}
</style>
