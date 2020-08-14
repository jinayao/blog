<template>
  <div class="Project">
    <ul>
      <li @click="handleSeclect">
        <div class="img">
          <img src="../../../public/4.png" alt width="100%" height="100%" />
        </div>
        <div class="des">
          <div class="title">
            <p>XXXXXX</p>
          </div>
          <div class="control">
            <button @click.stop="handleSupport()" :disabled="btn">
              <i class="el-icon-thumb"></i>
              点赞({{count}})
            </button>
            <span>发布时间 : 2020-06-05</span>
          </div>
        </div>
      </li>
    </ul>
    <el-pagination
      @size-change="handleSizeChange"
      @current-change="handleCurrentChange"
      :current-page.sync="currentPage"
      :page-size="10"
      layout="total, prev, pager, next, jumper"
      :total="100"
    ></el-pagination>
  </div>
</template>

<script>
export default {
  name: "Project",
  data() {
    return {
      currentPage: 1,
      count:0,
      btn:false
    };
  },
  components: {},
  methods: {
    handleSupport(e){
      this.count ++;
      this.btn=true
    },
    handleSizeChange(val) {
      console.log(`每页 ${val} 条`);
    },
    handleCurrentChange(val) {
      console.log(`当前页: ${val}`);
    },
    handleSeclect() {
      console.log(234);
      this.$emit("handleSeclect", false);
    },
  }
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
      transition: transform 0.3s;
      &:hover {
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
          height: 22px;
          line-height: 22px;
          justify-content: flex-end;
          color: #666;
          button {
            border: none;
            background: none;
            user-select: none;
            color: #666;
            font-size: inherit;
            cursor: pointer;
            &:hover {
              color: red;
            }
          }
          span{
            margin-top: 1px;
            margin-left: 20px;
          }
        }
      }
    }
  }
}
</style>
