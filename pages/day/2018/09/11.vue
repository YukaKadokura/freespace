<template>
    <div class="contents">
        <h1 class="title">{{ title }}</h1>
        <div class="content">
            <p class="midashi1">フォントの検証です。</p>
            <div>
                デフォルト：{{ moji }}
            </div>
            <div class="font1">
                sans-serif：{{ moji }}
            </div>
            <div class="font2">
                monospace：{{ moji }}
            </div>
            <div class="font3">
                ヒラギノ角ゴシック:{{ moji }}
            </div>
        </div>
        <div class="content">
            <p class="midashi1">色々な見出しです。</p>
            <div class="midashi2">見出し2</div>
            <div class="midashi3">見出し3</div>
            <div class="midashi4">見出し4</div>
            <div class="midashi5">見出し5</div>
            <div class="midashi6">見出し6</div>
            <div class="midashi7">見出し7</div>
            <div class="midashi8">見出し8</div>
            <div class="midashi9">
                <h1>見出し9</h1>
            </div>
            <div class="midashi10">見出し10</div>
        </div>
        <div class="content">
            <p class="midashi1">色々なリストです。</p>
            <ul class="list1">
                <li>リスト</li>
                <li>リスト</li>
                <li>リスト</li>
            </ul>
            <ul class="list2">
                <li>リスト</li>
                <li>リスト</li>
                <li>リスト</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180911",
            moji:"ABC123あいうえおアイウエオ"
        }
    }
}
</script>

<style scoped>
.contents{
    margin:10px;
}
.title{
    color:#202020;
}
.content{
    margin:10px;
}
.midashi1{
    padding-left:5px;
    border-left:solid #202020;
    padding-top:5px;
    padding-bottom:5px;
}
.font1{
    font-family:sans-serif;
}
.font2{
    font-family:monospace;
}
.font3{
    font-family:ヒラギノ角ゴシック;
}
.midashi2{
    color:royalblue;
    border-bottom:dashed 2px royalblue;
    padding-bottom:3px;
    width:50%;
    font-weight:bold;
    margin-top:5px;
}
.midashi3{
    border-bottom:double 5px orange;
    padding-bottom:3px;
    width:50%;
    font-weight:bold;
    color:#202020;
    margin-top:10px;
}
.midashi4{
    padding:5px;
    background:lightskyblue;
    width:50%;
    font-weight:bold;
    color:#202020;
    margin-top:10px;
}
.midashi5{
    padding:5px;
    background:lightskyblue;
    width:50%;
    color:#202020;
    margin-top:10px;
}
.midashi6{
    background:#DFEFFF;
    padding:10px;
    border:dashed 1px #96c2fe;
    color:#454545;
    width:50%;
    margin-top:10px;
}
.midashi7{
    background:#DFEFFF;
    padding:10px;
    border:dashed 1px #96c2fe;
    color:#454545;
    width:50%;
    box-shadow: 0px 0px 0px 5px #dfefff;
    margin-top:10px;
}
.midashi8{
    background:#DFEFFF;
    padding:10px;
    border:dashed 2px #96c2fe;
    color:#454545;
    width:50%;
    box-shadow: 0px 0px 0px 5px #dfefff;
    margin-top:15px;
}
.midashi9{
    margin-top:10px;
}
.midashi9 h1:first-letter{
    font-size:20px;
    color:lightskyblue;
}
.midashi9 h1{
    font-size:15px;
    color:#202020;
}
.midashi10{
    color:maroon;
    background:khaki;
    border-left:solid 5px gold;
    padding:10px;
    width:50%;
    font-weight:bold;
    margin-top:10px;
}
.list1{
    background:powderblue;
    width:50%;
    padding:5px;
    border:solid 2px grey;
}
.list1 li{
    margin-left:25px;
    padding:5px;
}
.list2{
    background:#dfefff;
    box-shadow: 0px 0px 0px 5px #dfefff;
    width:50%;
    padding:5px;
    border:dashed 2px dodgerblue;
    margin-top:15px;
}
.list2 li{
    margin-left:25px;
    padding:5px;
}
</style>