<template>
  <div class="Home">
首页  
  </div>
</template>

<script>
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

  }
};
</script>

<style lang="less" scoped>
.Home {
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,.3);
}
</style>
