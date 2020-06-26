<template>
  <div class="Project">
    <ul>
      <li>
        <div class="img">
          <img src="../../../public/4.png" alt width="100%" height="100%" />
        </div>
        <div class="des">
          <div class="title">
            <p>XXXXXX</p>
          </div>
          <div class="control">
            <span>
              <i class="el-icon-thumb"></i>
              点赞(22)
            </span>
            <span>发布时间 : 2020-06-05</span>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Project",
  components: {}
};
</script>

<style lang="less" scoped>
.Project {
  width: 800px;
  ul {
    li {
      display: flex;
      justify-content: space-around;
      height: 160px;
      padding: 10px 20px;
      margin-bottom: 20px;
      background: #ddd;
      border-radius: 8px;
      box-shadow: 8px 8px 8px 2px #666;
      cursor: pointer;
      transition: transform .3s;
      &:hover{
        transform: scale(1.02);
      }
      .img {
        display: inline-block;
        width: 160px;
        height: 160px;
        background: rosybrown;
        border-radius: 8px;
        overflow: hidden;
      }
      .des {
        display: flex;
        width: 500px;
        height: 100%;
        flex-direction: column;
        justify-content: space-between;
        .title {
          text-align: left;
          font-size: 44px;
          margin-top: 20px;
        }
        .control {
          display: flex;
          justify-content: flex-end;
          color: #666;
          span {
            margin-left: 20px;
            &:hover {
              color: red;
            }
          }
        }
      }
    }
  }
}
</style>
