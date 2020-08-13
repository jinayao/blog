<template>
  <div>
    <ul class="menu">
      <router-link v-for="item in menu" :key="item.path" :to="item.path" tag="li" class="menu-cell">
         <img class="menu-cell__image" :src="item.src">
        <div class="menu-cell__title">{{item.name}}</div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HeaderNav",
  props: ["menu"]
};
</script>

<style lang="less" scoped>
*,
*::before,
*::after {
  box-sizing: border-box;
}
.menu {
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  justify-content: center;
  align-items: center;
  max-width: 800px;
  margin: 0 auto;
  padding: 0;
  -webkit-transform: translateY(34.375px);
  transform: translateY(34.375px);
}
.menu-cell {
  flex: 0 1 190px;
  max-width: 190px;
  height: 100.5px;
  margin: 50px 10.5px 20px;
  position: relative;
  padding: 0.5em;
  text-align: center;
  background: #fff;
  color: #fff;
  z-index: 1;
  cursor: pointer;
  &:hover{
    .menu-cell__title{
      animation: changesize .5s linear;
    }
    .menu-cell__image{
      animation: changeimage .5s linear;
    }
  }
}
.menu-cell::before {
  background: #ddd;
  -webkit-transform: scale(1.055);
  transform: scale(1.055);
}
.menu-cell::after {
  background: #333;
  transition: opacity 350ms;
}
.menu-cell::before,
.menu-cell::after {
  content: "";
}
.menu-cell:hover::before {
  background: red;
  -webkit-transform: scale(1.055);
  transform: scale(1.055);
}
.menu-cell:hover::after {
  transition: opacity 350ms;
}
.menu__placeholder {
  display: none;
  opacity: 0;
  width: 250px;
  margin: 0 12.5px;
}
.menu-cell__image {
  width: 70px;
  height: 70px;
  margin-top: -10px;
  margin-bottom: 15px;
  -o-object-fit: cover;
  object-fit: cover;
  -o-object-position: center;
  object-position: center;
  border-style: none;
}

.menu-cell__title {
  height: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  -webkit-hyphens: auto;
  -ms-hyphens: auto;
  hyphens: auto;
  word-break: break-word;
  text-transform: uppercase;
  font-weight: 700;
  font-size: 1.35em;
  transition: opacity 350ms;
}
.menu-cell::before,
.menu-cell::after {
  top: -50%;
  left: 0;
  width: 100%;
  height: 200%;
  display: block;
  position: absolute;
  -webkit-clip-path: polygon(
    50% 0%,
    100% 25%,
    100% 75%,
    50% 100%,
    0% 75%,
    0% 25%
  );
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  z-index: -1;
}
@keyframes changesize{
  0%{
    transform: scale(1);
  }
  50%{
    transform: scale(1.5);
  }
  100%{
    transform: scale(1);
  }
}
@keyframes changeimage{
  0%{
    transform: scale(1);
  }
  50%{
    transform: scale(1.1);
  }
  100%{
    transform: scale(1);
  }
}
</style>