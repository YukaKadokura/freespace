<template>
    <div class="contents">
        <h1>{{ title }}</h1>
        <div class="content c1">
            <h2>おみくじ</h2>
            <div class="omikuji">
                ？
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180917"
        }
    }
}
</script>

<style scoped>
.contents{
    margin:5px;
}
.contents h1{
    font-size:20px;
}
.content{
    margin-top:20px;
}
.c1 h2{
    font-size:15px;
    color:#454545;
    padding:5px;
    border-left:solid 3px #454545;
}
.c1 .omikuji{
    margin-top:15px;
    width:200px;
    height:200px;
    border-radius:50%;
    background:red;
    text-align:center;
    padding:40px;
    color:white;
    font-weight:bold;
    font-size:30px;
}
</style>