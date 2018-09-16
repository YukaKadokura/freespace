<template>
    <div class="contents">
        <h1>{{ title }}</h1>
        <div class="content1">
            <h2>マウスオーバーすると少し右下に移動します。</h2>
            <div class="box">
            </div>
        </div>
        <div class="content2">
            <h2>見出し</h2>
            <div class="box">
            </div>
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
    /* 変形後のスタイル */
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
    transform: rotate(45deg);
}
</style>
