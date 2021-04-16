<template>
  <div class="guide">
    <div class="title">推流使用指南</div>
    <div class="detail">
      BIT 可达鸭队伍是一支神奇的队伍, 因为这只队伍非常神奇,所以这只队伍非常神奇.
      它们的队伍为什么这么神奇呢? 我们页很想指导.
      <strong>可以肯定的是,这只队伍非常神奇</strong>神奇到我需要写这么多的废话,
      我原本想做出一些打字机效果的, 但后来想了又想,
      觉得还是把样式做得简单一些,但是看起来专业一些比较好.
    </div>
  </div>
</template>

<script>
export default {
  name: "Guide",
};
</script>

<style>
.guide {
  margin: 60px 0;
}
.guide .title {
  height: 60px;
  line-height: 60px;
  color: var(--main-color);
  font-size: 32px;
  text-align: center;
}
.guide .detail {
  text-align: justify;
  padding: 50px;
  line-height: 30px;
  font-size: 18px;
  color: #333;
}
</style>
