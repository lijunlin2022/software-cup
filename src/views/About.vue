<template>
  <div class="about">
    <ul>
      <li v-for="(item, index) in urls" :key="item + index">
        <video controls="controls" autoplay muted :src="item"></video>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      urls: [
        "https://media.w3.org/2010/05/sintel/trailer.mp4",
        "http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4",
        "https://www.w3schools.com/html/movie.mp4",
      ],
    };
  },
};
</script>
<style scoped>
p {
  color: #fff;
  font-size: 20px;
  font-family: "Microsoft YaHei", Helvetica, Arial, sans-serif;
  font-weight: bold;
}
video {
  width: 50vw;
  display: block;
  object-fit: contain;
  margin: 25px auto;
}
@media screen and (max-width: 768px) {
  video {
    width: 95vw;
  }
}
</style>
