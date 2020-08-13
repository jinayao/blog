<template>
  <div class="Contact">
    <navbar></navbar>
    <div class="content">
      <ProjectNav :title="title"></ProjectNav>
      <div class="info">
        <div class="exMsg">
          <p>把握生命里的每一分钟，</p>
          <p>全力以赴心中的梦!</p>
        </div>
        <div class="authorInfo">
          <p>QQ:470945645</p>
          <p>邮箱:470945645@qq.com</p>
          <p>
            微信二维码:
            <img src="../assets/Wechat.jpeg" width="100%"/>
          </p>
        </div>
      </div>
      <span class="warn">注：添加好友请备注”源自博客“</span>
    </div>
  </div>
</template>

<script>
import ProjectNav from "../components/common/ProjectNav";
import navbar from "../components/common/narBar"
export default {
  name: "Contact",
  data() {
    return {
      title: "联系我"
    };
  },
  components: {
    ProjectNav,
    navbar
  }
};
</script>

<style lang="less" scoped>
.Contact {
  width: 100%;
  height: 100%;
  .content {
    width: 1180px;
    height: calc(100% - 40px);
    margin: auto;
    padding: 20px 0;
    background: url("../assets/what-we-do-bg.png") no-repeat 0 160px;
    .info {
      display: flex;
      margin-top: 130px;
      .exMsg{
        width: 600px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        transform: rotate(-20deg);
        p{
          font-size: 36px;
          line-height: 80px;
          color: #fff;
        }
      }
      .authorInfo {
        display: flex;
        flex-direction: column;
        padding-left: 40px;
        border-left: 2px solid #fff;
        p {
          margin: 20px 0;
          color: #fff;
          font-size: 20px;
          text-align: left;
          img{
            width: 180px;
            margin-left: 20px;
            vertical-align: top;
          }
        }
      }
    }
    .warn{
      line-height: 80px;
      color: red;
    }
  }
}
</style>
