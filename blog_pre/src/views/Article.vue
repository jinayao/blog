<template>
  <div class="Article">
    <div class="file">
      <div class="projectBox">
        <ProjectNav />
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
export default {
  name: "Article",
  components: {
    Project,
    Recommend,
    ProjectNav
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
      flex-direction: column;
      padding: 20px;
    }
  }
}
</style>
