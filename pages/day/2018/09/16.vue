<template>
    <div class="contents">
        <h1>{{ title }}</h1>
        <div class="content1">
            <h2>マウスオーバーすると少し右下に移動します。</h2>
            <div class="box">
            </div>
        </div>
        <div class="content2">
            <h2>マウスオーバーすると左に45度回転します。</h2>
            <div class="box">
            </div>
        </div>
        <div class="content3">
            <h2>マウスオーバーすると中心を起点に2倍に拡大します。</h2>
            <div class="box">
            </div>
        </div>
        <div class="content4">
            <h2>マウスオーバーすると0.4sかけて回転し不透明度を変更します。</h2>
            <div class="box"></div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180916"
        }
    }
}
</script>

<style scoped>
.contents{
    margin:20px;
}
.contents h1{
    font-size:20px;
}
.content1{
    margin-top:20px;
}
.content1 h2{
    font-size:15px;
    color:#454545;
    background:#dedede;
    box-shadow:0 0 0 5px #dedede;
    border: dashed 2px black;
    width:50%;
    padding:5px;
    margin-bottom:20px;
}
.content1 .box{
    width:40px;
    height:40px;
    background:skyblue;
    cursor: pointer;
}
.content1 .box:hover{
    /* x,y軸分移動 */
    transform: translate(10px, 20px);
}
.content2{
    margin-top:20px;
}
.content2 h2{
    font-size:15px;
    color:#454545;
    background:#f5f6ce;
    box-shadow:0 0 0 5px #f5f6ce;
    border: dashed 2px orange;
    width:50%;
    padding:5px;
    margin-bottom:20px;
}
.content2 .box{
    width:40px;
    height:40px;
    background:blue;
    cursor: pointer;
}
.content2 .box:hover{
    /* 45度回転 */
    transform: rotate(45deg);
}
.content3{
    margin-top:20px;
}
.content3 h2{
    font-size:15px;
    width:50%;
    padding:5px;
    color:#454545;
    background:#cef6f5;
    box-shadow:0 0 0 5px #cef6f5;
    border:dashed 2px skyblue;
    margin-bottom:20px;
}
.content3 .box{
    width:40px;
    height:40px;
    background:lightblue;
    cursor: pointer;
    margin:40px;
}
.content3 .box:hover{
    transform: scale(2);
}
.content4{
    margin-top:20px;
}
.content4 h2{
    font-size:15px;
    padding:5px;
    color: #454545;
    border-bottom:dashed 2px #454545;
    width:50%;
    margin-bottom:20px;
}
.content4 .box{
    width:40px;
    height:40px;
    background:mediumaquamarine;
    cursor: pointer;
}
.content4 .box:hover{
    /* transition-property: transform opacity; */
    /* transition-duration:.4s; */
    transition: all .4s;
    transform: rotate(45deg);
    opacity: .3;
}
</style>
