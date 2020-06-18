<template>
  <div class="Home">
    <HeaderNav></HeaderNav>
  </div>
</template>

<script>
import HeaderNav  from "../components/HeaderNav/HeaderNav"
export default {
  name: "Home",
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
