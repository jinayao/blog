<template>
  <div class="nav">
    <ul>
      <li v-for="(item,index) in menu" :key="index">
        <router-link :to="item.path">{{item.name}}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "nav",
  props:["menu"]
};
</script>

<style lang="less" scoped>
.nav{
  width: 100%;
  background-color: rgba(0, 0, 0,.2);
}
ul{
  width: 800px;
  height: 60px;
  display: flex;
  margin:auto;
  justify-content: space-around;
  li{
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-right: 40px;
  }
}
li a {
    display: block;
    font-size: 16px;
    text-align: center;
    padding: 10px 15px;
    line-height: 25px;
    color: #fff;
    text-decoration: none;
}
 
li a:hover {
    transform: rotate(5deg) scale(1.1);
}
li a:before, li a:after {
    opacity: 0;
    border-top: 1px solid #fff;
    content: '';
    display: block;
    position: relative;
    z-index: -1;
    margin: auto;
    width: 0px;
}
 
li a:before {
    top: 0px;
    transform: rotate(120deg) translateY(-50%) translateX(-50%);
}
 
li a:after {
    top: 5px;
    transform: rotate(-60deg) translateY(-50%) translateX(-50%);
}          
li a:hover:before, li a:hover:after{
    transition: all 0.3s ease;
    opacity: 1;
    width: 20px;
}        
</style>