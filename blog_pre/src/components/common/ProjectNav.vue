<template>
  <div class="projectNav">
    <div class="nav">
      <div class="title">{{title}}</div>
      <div class="type" v-if="NavData">
        <span>分类:</span>
        <ul>
          <li v-for="(item,index) in NavData" :key="index">{{item.name}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectNav",
  props: ["NavData","title"],
  computed: {
    // typeList(){
    //   return 
    // }
  }
};
</script>

<style lang="less" scoped>
.projectNav {
  width: 100%;
  margin-bottom: 30px;
  .nav {
    width: 100%;
    padding-bottom: 10px;
    border-bottom: 4px solid red;
    text-align: left;
    .title {
      margin-bottom: 20px;
      font-size: 26px;
      font-weight: bold;
      text-indent: 2px;
    }
    .type {
      display: flex;
      color: #999;
      &>span{
        font-size: 14px;
        line-height: 30px;
      }
      ul {
        display: flex;
        flex-wrap: wrap;
        li {
          width: 80px;
          height: 30px;
          margin: 0 10px 10px;
          text-align: center;
          line-height: 30px;
          font-size: 12px;
          border: 1px solid #999;
          border-radius: 8px;
          &:hover {
            cursor: pointer;
            color: red;
          }
        }
      }
    }
  }
}
</style>
