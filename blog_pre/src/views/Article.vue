<template>
  <div class="Article">
    <div class="file">
    <Project />
    <Recommend />
    </div>
  </div>
</template>

<script>
import Project from '../components/Project/Project';
import Recommend from '../components/Project/Recommend'
export default {
  name: "Article",
  components: {
    Project,
    Recommend
  }
};
</script>

<style lang="less" scoped>
.Article {
  width: 100%;
  .file{
  display: flex;
  width: 1180px;
  margin: auto;
  justify-content: space-around;
  }
}
</style>
