<template>
  <div class="home">
    <cube></cube>
    <typing-box></typing-box>
  </div>
</template>

<script>
import TypingBox from "@/components/typingBox/TypingBox.vue";
import Cube from "@/components/cube/Cube.vue";
export default {
  name: "Home",
  components: {
    TypingBox,
    Cube,
  },
};
</script>
