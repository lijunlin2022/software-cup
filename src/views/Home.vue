<template>
  <div class="home">
    <slogan></slogan>
    <introduction></introduction>
    <cube></cube>
    <guide></guide>
    <main-footer></main-footer>
  </div>
</template>

<script>
import Slogan from "@/components/content/slogan/Slogan.vue";
import Introduction from "@/components/content/introduction/Introduction.vue";
import Cube from "@/components/content/cube/Cube.vue";
import Guide from "@/components/content/guide/Guide.vue";
import MainFooter from "@/components/content/mainFooter/MainFooter.vue";
export default {
  name: "Home",
  components: {
    Slogan,
    Introduction,
    Cube,
    Guide,
    MainFooter,
  },
};
</script>
