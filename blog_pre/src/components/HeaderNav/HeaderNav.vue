<template>
  <div class="nav">
    <ul>
      <li>
        <a href="#">首页</a>
      </li>
      <li>
        <a href="#">不知道</a>
      </li>
      <li>
        <a href="#">不知道</a>
      </li>
      <li>
        <a href="#">不知道</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "nav"
};
</script>

<style lang="less" scoped>
ul{
  width: 800px;
  height: 80px;
  display: flex;
  margin: 10px auto;
  justify-content: flex-start;
  li{
    margin-right: 40px;
  }
}
li a {
    display: block;
    font-size: 20px;
    text-align: center;
    padding: 10px 15px;
    line-height: 25px;
    color: #777;
    text-decoration: none;
}
 
li a:hover {
    transform: rotate(5deg) scale(1.1);
}
li a:before, li a:after {
    opacity: 0;
    border-top: 1px solid #999;
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