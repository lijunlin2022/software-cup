<template>
  <div class="about">
    <ul>
      <li v-for="(item, index) in urls" :key="item + index">
        <div class="video-container">
          <video controls autoplay muted :src="item"></video>
          <button @click="deleteItem(index)">删除</button>
        </div>
      </li>
    </ul>
    <!-- 底部的输入推流地址按钮 -->
    <footer>
      <toggle-input>
        <template v-slot:input>
          <input type="text" placeholder="请输入推流地址" v-model="address" />
        </template>
        <template v-slot:btn>
          <button @click="addItem">确定</button>
        </template>
      </toggle-input>
    </footer>
  </div>
</template>

<script>
import ToggleInput from "@/components/common/toggleInput/ToggleInput.vue";
export default {
  name: "About",
  components: {
    ToggleInput,
  },
  data() {
    return {
      address: "",
      urls: ["https://media.w3.org/2010/05/sintel/trailer.mp4"],
      cnt: 1,
    };
  },
  methods: {
    addItem() {
      if (this.address === "") {
        alert("请输入合法的推流地址");
        return;
      }
      if (this.cnt >= 9) {
        alert("最多显示 9 个推流地址");
        return 0;
      }
      this.urls.push(this.address);
      this.address = "";
      this.cnt++;
    },
    deleteItem(index) {
      this.urls.splice(index, 1);
      this.cnt--;
      alert("删除成功");
    },
  },
};
</script>
<style scoped>
ul {
  text-align: center;
  /* 保证视频删除按钮不会被 footer 遮挡 */
  margin-bottom: 100px;
}
footer {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 10px;
}
ul li {
  display: inline-block;
  margin: 10px;
}
.video-container {
  width: 250px;
}
.video-container video {
  width: 100%;
}
.video-container button {
  display: block;
  width: 100%;
  height: 30px;
  background-color: var(--assist-color);
  border: none;
  outline: none;
  border-radius: 5px;
  color: #fff;
  font-size: 14px;
}
.video-container button:hover {
  background-color: var(--main-color);
}
@media screen and (min-width: 992px) {
  .video-container {
    width: 400px;
  }
}
</style>
