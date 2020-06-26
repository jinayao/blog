<template>
  <div class="Recommend">
    <div class="box">
      <RecommendBox :recommendData="recommendData"></RecommendBox>
    </div>
  </div>
</template>

<script>
import RecommendBox from "../common/Recommend-box"
export default {
  name: "Recommend",
  data(){
    return{
      recommendData:[
        {
          title:"热门推荐",
          data:[]
        },
        {
          title:"最近更新",
          data:[]
        },
        {
          title:"近期留言",
          data:[]
        }
      ]
    }
  },
  components: {
      RecommendBox
  }
};
</script>

<style lang="less" scoped>
.Recommend {
  width: 280px;
  .box {
    position: fixed;
    top: 20px;
    width: 280px;
  }
}
</style>