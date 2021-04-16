<template>
  <div class="toggle-input">
    <div class="navbar">
      <input type="checkbox" />
      <span></span><span></span>
      <div>
        <slot name="input"></slot>
        <slot name="btn"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ToggleInput",
};
</script>

<style scoped>
.toggle-input,
.navbar,
.navbar div {
  display: flex;
  justify-content: center;
  align-items: center;
}
.navbar {
  position: relative;
  padding: 10px;
  border-radius: 40px;
  background-color: var(--main-color);
}
.navbar input[type="checkbox"] {
  width: 35px;
  height: 35px;
  /* 直接变透明, 不会产生选择的效果 */
  opacity: 0;
}
.navbar span {
  position: absolute;
  left: 15px;
  top: calc(50% - 10px);
  width: 25px;
  height: 4px;
  background-color: #fff;
  /* span 覆盖了复选框 */
  /* 加上整个属性之后,原本的事件没有了,鼠标点击就可以激发复选框事件 */
  pointer-events: none;
  transition: transform 0.3s ease-out, top 0.3s ease-out;
}
.navbar input ~ div {
  width: 0;
  overflow: hidden;
  transition: all 0.5s ease-out;
}
.navbar span:last-of-type {
  top: calc(50% + 4px);
}
.navbar ::v-deep(input[type="text"]) {
  width: 80%;
  height: 40px;
  outline: none;
  border: none;
  border-radius: 15px;
  padding-left: 5px;
  color: #666;
  font-size: 14px;
}
.navbar ::v-deep(button) {
  display: block;
  width: 20%;
  height: 40px;
  margin-left: 5px;
  border-radius: 15px;
  background-color: #fff;
  outline: none;
  border: none;
  color: #666;
  font-size: 14px;
}
.navbar input:checked ~ div {
  width: 200px;
}
/* 选中时两条线旋转 */
.navbar input:checked ~ span:first-of-type {
  top: calc(50% - 2px);
  transform: rotate(-45deg);
  transition: top 0.3s ease-out, transform 0.3s ease-out;
}
.navbar input:checked ~ span:last-of-type {
  top: calc(50% - 2px);
  transform: rotate(45deg);
  transition: top 0.3s ease-out, transform 0.3s ease-out;
}
@media screen and (min-width: 992px) {
  .navbar input:checked ~ div {
    width: 500px;
  }
}
</style>
