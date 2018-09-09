<template>
    <div class="container">
        <h1 class="title">20180909</h1>
        <div class="content">
            <p class="midashi">円です。</p>
            <div class="circle"></div>
        </div>
        <div class="content">
            <p class="midashi2">三角形です。</p>
            <div class="flex">
                <div class="triangle margin5"></div>
                <div class="triangle2 margin5"></div>
                <div class="triangle3 margin5"></div>
                <div class="triangle4 margin5"></div>
            </div>
        </div>
        <div class="content">
            <p class="midashi3">見出し</p>
        </div>
    </div>
</template>

<style scoped>
.container{
    margin:10px;
    padding:20px;
}
.title{
    color:#202020;
}
.content{
    pargin:10px;
    padding:10px;
    margin-bottom:20px;
}
.midashi{
    font-weight:bold;
    color:#6594e0;
    border-bottom:dashed 2px #6594e0;
    padding:10px;
}
.circle{
    width:100px;
    height:100px;
    border-radius:50%;
    background:teal;
}
.midashi2{
    font-weight:bold;
    background:#c2edff;
    padding:10px;
}
.flex{
    display:flex;
}
.margin5{
    margin-right:5px;
}
.triangle{
    width:0;
    height:0;
    border-left:25px solid transparent;
    border-right:25px solid transparent;
    border-bottom:50px solid #81C7D4;
}
.triangle2{
    width:0;
    height:0;
    border-bottom:25px solid transparent;
    border-top:25px solid transparent;
    border-right:50px solid #81C7D4;
}
.triangle3{
    width:0;
    height:0;
    border-top:25px solid transparent;
    border-bottom:25px solid transparent;
    border-left:50px solid #81c7d4;
}
.triangle4{
    wigth:0;
    height:0;
    border-left:25px solid transparent;
    border-right:25px solid transparent;
    border-top:50px solid #81c7d4;
}
.midashi3{
    color:#494949;
    font-weight:bold;
    background:transparent;
    border-left:solid 5px #7db4e6;
    padding:10px;
}
</style>