<template>
  <div class="Recommend-box">
    <h3 class="title">XXXXXX</h3>
    <ul>
      <li>XXXXXXXXXXX</li>
      <li>XXXXXXXXXXX</li>
      <li>XXXXXXXXXXX</li>
      <li>XXXXXXXXXXX</li>
      <li>XXXXXXXXXXX</li>
    </ul>
    <div class="control">
      <span>
        更多
        <i class="el-icon-d-arrow-right"></i>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Recommend-box"
};
</script>

<style lang="less" scoped>
.Recommend-box {
  height: 185px;
  padding: 20px;
  margin-bottom: 20px;
  border: 1px solid black;
  border-radius: 8px;
  text-align: left;
  .title {
    font-size: 22px;
    &::after {
      content: "";
      display: block;
      width: 100%;
      border: 1px solid #999;
      margin: 10px 0;
    }
  }
  ul {
    font-size: 16px;
    color: #999;
    li {
      margin: 10px 0;
      &:hover {
        color: red;
        cursor: pointer;
        text-decoration: underline;
      }
    }
  }
  .control {
    text-align: right;
    &:hover {
      color: red;
      cursor: pointer;
      text-decoration: underline;
    }
  }
}
</style>