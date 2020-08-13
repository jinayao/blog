<template>
  <div class="Home">
    <navbar></navbar>
  </div>
</template>

<script>
import navbar from "../components/common/narBar";
export default {
  name: "Home",
  data() {
    return {

    };
  },
  components: {
    navbar
  }
};
</script>

<style lang="less" scoped>
.Home {
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.3);
}
</style>
