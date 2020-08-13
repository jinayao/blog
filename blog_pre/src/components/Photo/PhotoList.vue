<template>
  <div class="PhotoList">
    <el-page-header class="listHeader" @back="goBack" content="小刘鸭集锦"></el-page-header>
    <ul>
      <li>
        <img src="../../../public/4.png" width="100%" height="100%" alt />
        <div class="title">XXXX</div>
      </li>
      <li>
        <img src="../../../public/4.png" width="100%" height="100%" alt />
        <div class="title">XXXX</div>
      </li>
      <li>
        <img src="../../../public/4.png" width="100%" height="100%" alt />
        <div class="title">XXXX</div>
      </li>
      <li>
        <img src="../../../public/4.png" width="100%" height="100%" alt />
        <div class="title">XXXX</div>
      </li>
      <li>
        <img src="../../../public/4.png" width="100%" height="100%" alt />
        <div class="title">XXXX</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PhotoList",
  data() {
    return {};
  },
  components: {},
  methods: {
      goBack(){
          this.$emit('goBack')
      }
  }
};
</script>

<style lang="less">
.PhotoList {
  width: 100%;
  .listHeader{
      color: #999;
      margin-bottom: 20px;
  }
  .el-page-header__content{
      color: #999 !important;
  }
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 100%;
    li {
      width: 180px;
      margin-bottom: 20px;
      transition: all 0.2s linear;
      &:hover {
        cursor: pointer;
        transform: scale(1.03);
      }
      img {
        width: 180px;
        height: 180px;
      }
      .title {
        margin-top: 10px;
        font-size: 18px;
      }
    }
  }
}
</style>
