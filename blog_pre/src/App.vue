<template>
  <div id="app">
    <transition :name="transitionName">
      <router-view />
    </transition>
  </div>
</template>

 <script>
export default {
  name: "App",
  data() {
    return {
      transitionName: ""
    };
  },
  watch: {
    // 使用watch 监听$router的变化
    $route(to, from) {
      // 如果to索引大于from索引,判断为前进状态,反之则为后退状态
      if (to.meta.index > from.meta.index) {
        // 设置动画名称
        this.transitionName = "slide-enter";
      } else {
        this.transitionName = "slide-leave";
      }
    }
  }
};
</script>

<style lang="less">
body,html,#app{
  width: 100%;
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 12px;
}
.slide-leave-enter-active,
.slide-leave-leave-active,
.slide-enter-enter-active,
.slide-enter-leave-active {
  will-change: transform;
  transition: transform 0.5s;
  position: absolute;
}
.slide-enter-enter {
  opacity: 1;
  transform: translate3d(0,-100%,0);
}
.slide-enter-leave-active {
  transform: translate3d(0,100%,0);
  opacity: 0;
}
.slide-leave-enter {
  transform: translate3d(0,100%,0);
  opacity: 0;
}
.slide-leave-leave-active {
  transform: translate3d(0,-100%,0);
  opacity: 1;
}

</style>
