<template>
  <div class="PhotoFile">
    <div class="file" @click="handleSeclect">
      <div class="photoCover">
        <img src="../../../public/4.png" width="100%" height="100%" alt />
      </div>
      <div class="title">小刘鸭集锦</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PhotoFile",
  data() {
    return {};
  },
  components: {},
  methods: {
    handleSeclect() {
      console.log(234);
      this.$emit("handleSeclect", false);
    }
  }
};
</script>

<style lang="less" scoped>
.PhotoFile {
  position: relative;
  margin-bottom: 28px;
  &:hover {
    cursor: pointer;
    &:after {
      box-shadow: 2px -1px 2px #bbb;
    }
  }
  &:after,
  &:before {
    content: "";
    position: absolute;
    left: 5px;
    top: 5px;
    width: 210px;
    height: 210px;
    z-index: -1;
  }
  &:after {
    left: 10px;
    top: 10px;
    z-index: -2;
    box-shadow: 2px -1px 2px #ddd;
  }
  &:after,
  &:before,
  .photoCover {
    border: 2px solid #ddd;
    background-color: #fff;
    border-radius: 8px;
  }
  .photoCover {
    width: 200px;
    height: 200px;
    padding: 5px;
    z-index: 99;
    img {
      border-radius: 8px;
    }
  }
  .title {
    margin-top: 28px;
    font-size: 22px;
  }
}
</style>
