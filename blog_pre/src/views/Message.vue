<template>
  <div class="Message">
    <navbar></navbar>
    <div class="msgBox">
      <ProjectNav :title="title"></ProjectNav>
      <el-input type="textarea" rows="5" resize="none" placeholder="请输入留言" v-model="textarea2"></el-input>
      <div class="btn">
        <el-button type="primary" round>提交留言</el-button>
      </div>
    </div>
    <div class="list">
      <div class="msgTitle">留言详情:</div>
      <ul>
        <li v-for="item in 4">
          <div class="msg">
            <p class="msgPeople">
              <span>小明</span>
            </p>
            <p
              class="msgInfo"
            >你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好</p>
            <p class="msgTime">2020-05-01</p>
          </div>
          <div class="msgRes">
            <p class="author">
              <span>回复：</span>
            </p>
            <p
              class="resInfo"
            >你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好</p>
            <p class="resTime">2020-05-01</p>
          </div>
        </li>
      </ul>
    </div>
    <el-pagination
      @size-change="handleSizeChange"
      @current-change="handleCurrentChange"
      :current-page="currentPage"
      :page-size="10"
      layout="total, prev, pager, next, jumper"
      :total="40"
    ></el-pagination>
  </div>
</template>

<script>
import ProjectNav from "../components/common/ProjectNav";
import navbar from "../components/common/narBar"
export default {
  name: "Message",
  data() {
    return {
      title: "留言",
      textarea2: "",
      currentPage: 1
    };
  },
  methods: {
    handleSizeChange(val) {
      console.log(`每页 ${val} 条`);
    },
    handleCurrentChange(val) {
      console.log(`当前页: ${val}`);
    }
  },
  components: {
    ProjectNav,
    navbar
  }
};
</script>

<style lang="less" scoped>
.Message {
  width: 100%;
  padding-bottom: 40px;
  .msgBox {
    width: 1180px;
    margin: auto;
    padding: 20px 0;
    border-bottom: 1px dashed #ddd;
    .btn {
      text-align: left;
      margin-top: 10px;
    }
  }
  .list {
    width: 1180px;
    margin: auto;
    margin-top: 20px;
    text-align: left;
    font-size: 14px;
    color: #999;
    .msgTitle {
      margin-bottom: 20px;
      font-size: 16px;
      font-weight: bold;
      color: #000;
    }
    li {
      padding: 10px 0;
      border-bottom: 1px dashed #ddd;
      .msg {
        display: flex;
        .msgPeople {
          display: flex;
          flex-shrink: 0;
          flex-direction: column;
          justify-content: center;
          width: 140px;
          text-align: center;
          font-size: 16px;
          color: #000;
          border-right: 1px solid #ddd;
        }
        .msgInfo {
          padding: 20px 40px 20px 20px;
          flex-grow: 1;
        }
        .msgTime {
          display: flex;
          flex-shrink: 0;
          flex-direction: column;
          justify-content: center;
          width: 100px;
        }
      }
      .msgRes {
        display: flex;
        margin-left:160px;
        padding:10px 0;
        background-color: #ddd;
        .author{
          display: flex;
          width: 60px;
          flex-shrink: 0;
          flex-direction: column;
          justify-content: center;
          text-align: center;
          font-size: 14px;
          color: #000;
        }
        .resInfo{
          flex-grow: 1;
          padding-right:40px;
        }
        .resTime{
          display: flex;
          flex-shrink: 0;
          flex-direction: column;
          justify-content: center;
          width: 100px;
        }
      }

      &:last-of-type {
        border-bottom: none;
      }
    }
  }
}
</style>
