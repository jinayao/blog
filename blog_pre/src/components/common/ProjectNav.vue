<template>
    <div class="projectNav">
        <div class="nav">
            <div class="title">
                文章列表
            </div>
            <ul>
                <li v-for="(item,index) in NavData" :key="index">{{item.name}}</li>

            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name:"ProjectNav",
    props: ["NavData"]
}
</script>

<style lang="less" scoped>
    .projectNav{
        width: 100%;
        margin-bottom: 30px;
        .nav{
            width: 100%;
            padding-bottom:10px ;
            border-bottom: 4px solid red;
            text-align: left;
            .title{
                margin-bottom: 20px;
                font-size: 26px;
                font-weight: bold;
                text-indent: 2px;
            }
            ul{
                display: flex;
                flex-wrap: wrap;
                li{ 
                    width: 80px;
                    height: 30px;
                    margin:0 10px 10px;
                    text-align: center;
                    line-height: 30px;
                    font-size: 12px;
                    color: #999;
                    border: 1px solid #999;
                    border-radius: 8px;
                    &:hover{
                        cursor: pointer;
                        color: red;
                    }
                }
            }
        }
    }
</style>
