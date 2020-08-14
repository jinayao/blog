<template>
  <div class="articalInfo">
    <el-page-header class="listHeader" @back="goBack" content="文章详情"></el-page-header>
    <p class="title">你好</p>
    <div class="info">
      <p>asdasdasdads</p>
      <img src="../../assets/what-we-do-bg.png" alt />
    </div>
  </div>
</template>

<script>
export default {
  name: "articalInfo",
  methods: {
    goBack() {
      this.$emit("goBack");
    }
  }
};
</script>

<style scoped lang='less'>
.articalInfo {
  width: 100%;
  overflow: hidden;
  color: #000;
  .listHeader {
    color: #999;
  }
  .title{
      font-size: 20px;
      font-weight: bold;
      line-height: 40px;
  }
  .info{
      font-size: 14px;
      line-height: 28px;
      text-align: left;
  }
}
</style>