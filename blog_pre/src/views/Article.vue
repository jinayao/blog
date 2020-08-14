<template>
  <div class="Article">
    <navbar></navbar>
    <div class="file">
      <div class="projectBox">
        <ProjectNav :NavData="NavData" :title="title"/>
        <Project v-if="show" @handleSeclect='selectShow'/>
        <ArticalInfo v-else @goBack="goBack"></ArticalInfo>
      </div>
      <Recommend />
    </div>
  </div>
</template>

<script>
import ProjectNav from "../components/common/ProjectNav";
import Project from "../components/Project/Project";
import Recommend from "../components/Project/Recommend";
import navbar from "../components/common/narBar";
import ArticalInfo from "../components/Project/ArticalInfo"
export default {
  name: "Article",
  data(){
    return{
      title:'文章列表',
      NavData:[
        {
          name:"Javascript",
          path:"",
        },
        {
          name:"Vue",
          path:"",
        },
        {
          name:"React",
          path:"",
        },
        {
          name:"Node",
          path:"",
        },
        {
          name:"Mongo",
          path:"",
        },
        {
          name:"Three.js",
          path:"",
        },
      ],
      show:true
    }
  },
  components: {
    Project,
    Recommend,
    ProjectNav,
    navbar,
    ArticalInfo
  },
  methods: {
    selectShow(){
      this.show = false
    },
    goBack(){
      this.show = true
    }
  }
};
</script>

<style lang="less" scoped>
.Article {
  width: 100%;
  .file {
    display: flex;
    width: 1180px;
    margin: auto;
    justify-content: space-around;
    .projectBox{
      display: flex;
      width: 800px;
      flex-direction: column;
      padding: 20px;
    }
  }
}
</style>
