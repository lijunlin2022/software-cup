<template>
  <div class="introduction">
    <div class="triangle-top"></div>
    <div class="container">
      <p>团队成员</p>
      <div class="card-container">
        <div class="card">
          <div class="card-inner">
            <img src="../../../assets/img/teacher.png" alt="" />
            <p>XXX</p>
            <p>了解更多→</p>
          </div>
        </div>
        <div class="card">
          <div class="card-inner">
            <img src="../../../assets/img/student1.png" alt="" />
            <p>XXX</p>
            <p>了解更多→</p>
          </div>
        </div>
        <div class="card">
          <div class="card-inner">
            <img src="../../../assets/img/student2.png" alt="" />
            <p>XXX</p>
            <p>了解更多→</p>
          </div>
        </div>
        <div class="card">
          <div class="card-inner">
            <img src="../../../assets/img/student3.png" alt="" />
            <p>XXX</p>
            <p>了解更多→</p>
          </div>
        </div>
      </div>
    </div>
    <div class="triangle-bottom"></div>
  </div>
</template>

<script>
export default {
  name: "Introduction",
};
</script>

<style scoped>
.introduction {
  position: relative;
  height: 1000px;
}
.triangle-top,
.triangle-bottom {
  position: absolute;
  width: 60px;
  height: 60px;
  background-color: var(--assist-color);
  transform: rotate(45deg);
  color: #fff;
  left: calc(50% - 30px);
}
.triangle-top {
  top: -30px;
}
.triangle-bottom {
  bottom: 70px;
}
.introduction .container {
  width: 100%;
  height: 900px;
  background: url(../../../assets/img/bg9.jpg) center no-repeat;
  background-size: cover;
}
.introduction .container > p {
  padding: 60px;
  height: 60px;
  line-height: 60px;
  color: #fff;
  font-size: 32px;
  text-align: center;
}
.card-container {
  text-align: center;
}
.card {
  display: inline-block;
  width: 250px;
  height: 150px;
  margin: 10px;
  background: var(--assist-color);
}
.card-inner {
  height: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.card-inner > img {
  width: 100px;
  height: 100px;
}
.card-inner p:nth-of-type(1) {
  color: #fff;
  font-size: 20px;
}
.card-inner p:last-of-type {
  color: #fff;
  font-size: 14px;
}
@media screen and (min-width: 992px) {
  .introduction {
    height: 750px;
  }
  .introduction .container {
    height: 650px;
  }
  .card {
    height: 200px;
  }
  .card-inner {
    flex-direction: column;
    flex-wrap: wrap;
  }
}
</style>
