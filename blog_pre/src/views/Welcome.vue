<template>
  <div class="Welcome">
    <div class="content__title-wrap">
      <div class="wrapper">
        <h1 data-heading="学习无止步，进步无止息">学习无止步，进步无止息</h1>
      </div>
      <router-link to="/home" class="content__link">欢迎进入我的博客</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Welcome",
  components: {}
};
</script>

<style lang="less" scoped>
.Welcome {
  position: relative;
  width: 100vw;
  height: 100vh;
  background: #444;
  align-items: center;
  .content__title-wrap {
    position: absolute;
    width: 100%;
    white-space: nowrap;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    pointer-events: none;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    a {
      pointer-events: auto;
    }
    .content__title {
      font-size: 6vw;
      font-weight: normal;
      margin: 0.5rem 0 1.5rem;
      font-family: azo-sans-uber, sans-serif;
    }

    .content__link {
      position: absolute;
      top: 100px;
      transform: translateX(-50%);
      text-decoration: underline;
      font-family: azo-sans-uber, sans-serif;
      font-size: 1.1rem;
      color: #fff;
    }
    .wrapper {
      width: 100%;
      font-family: "Source Code Pro", monospace;
      margin: 0 auto;
      height: 100%;
      h1 {
        text-transform: uppercase;
        transform: translate(-50%, -100%) skew(10deg) rotate(-10deg);
        font-size: 7vw;
        top: 50%;
        left: 50%;
        margin: 0;
        position: absolute;
        text-rendering: optimizeLegibility;
        font-weight: 900;
        color: rgba(red, 0.7);
        white-space: nowrap;
        animation: fireDiv 1s infinite;
        &:before {
          content: attr(data-heading);
          position: absolute;
          left: 0;
          top: -4.8%;
          overflow: hidden;
          width: 100%;
          height: 50%;
          color: #fbf7f4;
          transform: translate(0.5vw, 0) skew(-13deg) scale(1, 1.2);
          z-index: 2;
          text-shadow: 2px -1px 6px rgba(0, 0, 0, 0.2);
        }

        &:after {
          content: attr(data-heading);
          position: absolute;
          left: 0;
          top: 0;
          overflow: hidden;
          width: 100%;
          height: 100%;
          z-index: 1;
          color: #d3cfcc;
          transform: translate(0vw, 0) skew(13deg) scale(1, 0.8);
          clip-path: polygon(0 50%, 100% 50%, 100% 100%, 0% 100%);
          text-shadow: 2px -1px 6px rgba(0, 0, 0, 0.3);
        }
      }
    }
  }
}
@keyframes fireDiv {
        0% {
          text-shadow: 0 0 4px white, 0 -5px 4px #ff3, 2px -10px 6px #fd3,
            -2px -15px 11px #f80, 2px -25px 18px #f20;
        }
        25% {
          text-shadow: 0 0 4px white, 2px -7px 6px #ff3, 2px -12px 8px #fd3,
            -3px -20px 11px #f80, 4px -30px 22px #f20;
        }
        50% {
          text-shadow: 0 0 4px white, 2px -10px 8px #ff3, 2px -14px 10px #fd3,
            -4px -25px 11px #f80, 4px -35px 25px #f20;
        }
        75% {
          text-shadow: 0 0 4px white, 2px -7px 6px #ff3, 2px -12px 8px #fd3,
            -3px -20px 11px #f80, 4px -30px 22px #f20;
        }
        100% {
          text-shadow: 0 0 4px white, 0 -5px 4px #ff3, 2px -10px 6px #fd3,
            -2px -15px 11px #f80, 2px -25px 18px #f20;
        }
      }

</style>
