<template>
  <div class="menuHolder">
    <div class="menuWindow">
      <ul class="p1">
        <li class="s1">
          <a>导航</a>
          <ul class="p2">
            <li class="s2" v-for="(item,index) in menu" :key="index">
              <router-link :to="item.path">{{item.name}}</router-link>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      menu: [
        {
          name: "首页",
          path: "/home"
        },
        {
          name: "文章",
          path: "/article"
        },
        {
          name: "相册",
          path: "/photo"
        },
        {
          name: "留言",
          path: "/message"
        },
        {
          name: "联系我",
          path: "/contact"
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.menuHolder {
  width: 70px;
  height: 70px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;

  .menuWindow {
    width: 80px;
    height: 80px;
    overflow: hidden;
    position: absolute;
    left: 0;
    top: 0;
    z-index: 100;
    -webkit-transition: 0s 1s;
    -moz-transition: 0s 1s;
    -ms-transition: 0s 1s;
    -o-transition: 0s 1s;
    transition: 0s 1s;
    ul {
      padding: 0;
      margin: 0;
      list-style: none;
      position: absolute;
      left: 0;
      top: 0;
      width: 0;
      height: 0;
      li {
        border-radius: 0 0 140px 0;
        width: 0;
        height: 0;
        a {
          color: #000;
          text-decoration: none;
          font: bold 13px/30px arial, sans-serif;
          text-align: center;
          box-shadow: -5px 5px 5px rgba(0, 0, 0, 0.4);
          -webkit-transform-origin: 0 0;
          -moz-transform-origin: 0 0;
          -ms-transform-origin: 0 0;
          -o-transform-origin: 0 0;
          transform-origin: 0 0;
        }
        &.s1 > a {
          user-select: none;
          position: absolute;
          display: block;
          width: 70px;
          height: 70px;
          background: #c8c8c8;
          font-size: 16px;
          text-align: left;
          text-indent: 10px;
          line-height: 60px;
          border-radius: 0 0 70px 0;
        }
        &.s2 > a {
          position: absolute;
          display: block;
          width: 70px;
          padding-left: 70px;
          height: 140px;
          background: #ddd;
          border-radius: 0 0 140px 0;
        }
        &:hover > a {
          background: #f00;
          color: #fff;
        }
      }
      &.p1 {
        li {
          position: absolute;
          left: 0;
          top: 0;
        }
      }
      &.p2,
      &.p3 {
        z-index: -1;
      }
      ul {
        -webkit-transform-origin: 0 0;
        -moz-transform-origin: 0 0;
        -ms-transform-origin: 0 0;
        -o-transform-origin: 0 0;
        transform-origin: 0 0;
        -webkit-transform: rotate(90deg);
        -moz-transform: rotateZ(90deg);
        -ms-transform: rotate(90deg);
        -o-transform: rotate(90deg);
        transform: rotate(90deg);
        -webkit-transition: 1s;
        -moz-transition: 1s;
        -ms-transition: 1s;
        -o-transition: 1s;
        transition: 1s;
      }
    }
  }
  &:hover .menuWindow {
    width: 150px;
    height: 150px;
    -webkit-transition: 0s 0s;
    -moz-transition: 0s 0s;
    -ms-transition: 0s 0s;
    -o-transition: 0s 0s;
    transition: 0s 0s;
  }
}
.menuHolder li.s2:nth-of-type(5) > a {
  background: #999;
  -webkit-transform: rotate(72deg);
  -moz-transform: rotateZ(72deg);
  -ms-transform: rotate(72deg);
  -o-transform: rotate(72deg);
  transform: rotate(72deg);
}
.menuHolder li.s2:nth-of-type(4) > a {
  background: #aaa;
  -webkit-transform: rotate(54deg);
  -moz-transform: rotateZ(54deg);
  -ms-transform: rotate(54deg);
  -o-transform: rotate(54deg);
  transform: rotate(54deg);
}
.menuHolder li.s2:nth-of-type(3) > a {
  background: #bbb;
  -webkit-transform: rotate(36deg);
  -moz-transform: rotateZ(36deg);
  -ms-transform: rotate(36deg);
  -o-transform: rotate(36deg);
  transform: rotate(36deg);
}
.menuHolder li.s2:nth-of-type(2) > a {
  background: #ccc;
  -webkit-transform: rotate(18deg);
  -moz-transform: rotateZ(18deg);
  -ms-transform: rotate(18deg);
  -o-transform: rotate(18deg);
  transform: rotate(18deg);
}
.menuHolder li.s1:hover ul.p2 {
  -webkit-transform: rotate(0deg);
  -moz-transform: rotateZ(0deg);
  -ms-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
}
</style>