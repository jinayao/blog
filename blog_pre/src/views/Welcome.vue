<template>
  <div class="Welcome">
    <div class="line"></div>
    <div class="des">
      <h1>欢迎来到我的博客</h1>
      <p>以下是快捷入口</p>
    </div>
    <HeaderNav :menu="menu"></HeaderNav>
  </div>
</template>

<script>
import one from "../../public/1.jpg"
import two from "../../public/4.png"
import three from "../../public/2.jpg"
import four from "../../public/3.jpeg"
import five from "../../public/5.png"
import HeaderNav from "../components/HeaderNav/HeaderNav";
export default {
  name: "Welcome",
  data() {
    return {
      menu: [
        {
          name: "首页",
          path: "/home",
          src:one
        },
        {
          name: "文章",
          path: "/article",
          src:two
        },
        {
          name: "相册",
          path: "/photo",
          src:three
        },
        {
          name: "留言",
          path: "/message",
          src:four
        },
        {
          name: "联系我",
          path: "/contact",
          src:five
        }
      ]
    };
  },
  components: {
    HeaderNav
  }
};
</script>

<style lang="less" scoped>
.Welcome {
  width: 100%;
  height: 100%;
  background-color: #333;
  .line{
    padding-top: 50px;
    margin-bottom: 50px;
    border-bottom: 10px solid red;
  }
  .des {
    
    h1 {
      margin-bottom: 30px;
      font-size: 44px;
      color: #fff;
    }
    p{
      margin-bottom: 20px;
      font-size: 20px;
      font-weight: bold;
      color: #999;
    }
  }
}
</style>
