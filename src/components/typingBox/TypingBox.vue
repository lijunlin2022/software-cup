<template>
  <div class="typing-box"></div>
</template>

<script>
export default {
  name: "TypingBox",
  data() {
    return {
      str:
        "嗟乎！时运不齐，命途多舛。冯唐易老，李广难封。屈贾谊于长沙，非无圣主；窜梁鸿于海曲，岂乏明时？所赖君子见机，达人知命。老当益壮，宁移白首之心？穷且益坚，不坠青云之志。酌贪泉而觉爽，处涸辙以犹欢。北海虽赊，扶摇可接；东隅已逝，桑榆非晚。孟尝高洁，空余报国之情；阮籍猖狂，岂效穷途之哭！",
    };
  },
  mounted() {
    let box = document.getElementsByClassName("typing-box")[0];
    let i = 0;
    box.innerText = "";
    let typing = setInterval(() => {
      box.innerText += this.str[i++];
      i >= this.str.length && clearInterval(typing);
    }, 100);
  },
};
</script>
<style scoped>
.typing-box {
  width: 70vw;
  margin: 5vh auto;
  color: #fff;
  font-size: 1em;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
