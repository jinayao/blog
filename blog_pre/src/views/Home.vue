<template>
  <div class="Home">
    <HeaderNav :menu="menu"></HeaderNav>
  </div>
</template>

<script>
import HeaderNav  from "../components/HeaderNav/HeaderNav"
export default {
  name: "Home",
  data(){
    return{
      menu:[
        {
          name:"首页",
          path:"/home"
        },
        {
          name:"文章",
          path:"/article"
        },
        {
          name:"相册",
          path:"/photo"
        },
        {
          name:"留言",
          path:"/message"
        },
        {
          name:"联系我",
          path:"/contact"
        },
      ]
    }
  },
  components: {
    HeaderNav
  }
};
</script>

<style lang="less" scoped>
.Home {
  width: 100%;
  height: 100%;
  background: url("../assets/what-we-do-bg.png") no-repeat 50% 50%;
}
</style>
