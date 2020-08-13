<template>
  <div class="Article">
    <navbar></navbar>
    <div class="file">
      <div class="projectBox">
        <ProjectNav :NavData="NavData" :title="title"/>
        <Project />
      </div>
      <Recommend />
    </div>
  </div>
</template>

<script>
import ProjectNav from "../components/common/ProjectNav";
import Project from "../components/Project/Project";
import Recommend from "../components/Project/Recommend";
import navbar from "../components/common/narBar"
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
      ]
    }
  },
  components: {
    Project,
    Recommend,
    ProjectNav,
    navbar
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
