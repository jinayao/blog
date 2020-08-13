<template>
  <div class="Photo">
    <navbar></navbar>
    <div class="content">
      <div class="projectBox">
        <ProjectNav :title="title" />
        <div v-if="show" class="list" >
          <PhotoFile @handleSeclect='selectShow'></PhotoFile>
        </div>
        <PhotoList v-else @goBack="goBack"></PhotoList>
      </div>
      <Recommend />
    </div>
  </div>
</template>

<script>
import ProjectNav from "../components/common/ProjectNav";
import Recommend from "../components/Project/Recommend";
import PhotoFile from "../components/Photo/PhotoFile";
import PhotoList from "../components/Photo/PhotoList";
import navbar from "../components/common/narBar"
export default {
  name: "Photo",
  data() {
    return {
      title: "相册",
      show:true
    };
  },
  components: {
    ProjectNav,
    Recommend,
    PhotoFile,PhotoList,
    navbar
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
.Photo {
  width: 100%;
  .content {
    display: flex;
    width: 1180px;
    margin: auto;
    justify-content: space-around;
    .projectBox {
      display: flex;
      width: 800px;
      flex-direction: column;
      padding: 20px;
      .list{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
      }
    }
  }
}
</style>
