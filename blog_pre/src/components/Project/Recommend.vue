<template>
  <div class="Recommend">
    <div class="box">
      <RecommendBox></RecommendBox>
      <RecommendBox></RecommendBox>
      <RecommendBox></RecommendBox>
    </div>
  </div>
</template>

<script>
import RecommendBox from "../common/Recommend-box"
export default {
  name: "Recommend",
  components: {
      RecommendBox
  }
};
</script>

<style lang="less" scoped>
.Recommend {
  width: 300px;
  .box {
    position: fixed;
    top: 20px;
    width: 300px;
  }
}
</style>