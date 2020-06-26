<template>
    <div class="projectNav">
        <div class="nav">
            <div class="title">
                文章列表
            </div>
            <ul>
                <li>html</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name:"ProjectNav",
    
}
</script>

<style lang="less" scoped>
    .projectNav{
        width: 100%;
        margin-bottom: 30px;
        .nav{
            width: 100%;
            padding-bottom:20px ;
            border-bottom: 4px solid red;
            text-align: left;
            .title{
                margin-bottom: 20px;
                font-size: 26px;
                font-weight: bold;
                text-indent: 2px;
            }
            ul{
                li{
                    width: 80px;
                    height: 30px;
                    text-align: center;
                    line-height: 30px;
                    font-size: 14px;
                    color: #666;
                    border: 1px solid #666;
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
