<template>
    <div class="MainContent">
        <h1>20180906</h1>
        <div class="SubContent">
            <div class="BorderBoxes">
                <div class="BorderBox1">
                    45degのdiv
                </div>
                <div class="BorderBox2">
                    90degのdiv
                </div>
                <div class="BorderBox3">
                    0degのdiv
                </div>
                <div class="BorderBox4">
                    135degのdiv
                </div>
                <div class="BorderBox5">
                    20px,40pxのdiv
                </div>
            </div>
        </div>
        <div class="SubContent">
            <p>//擬似要素:beforeの検証です。</p>
            <p class="giji1">擬似要素:before</p>
            <p>//擬似要素:afterの検証です。</p>
            <p class="giji2">擬似要素:after</p>
        </div> 
        <div class="SubContent">
            <p>//displayプロパティの検証です。</p>
            <p>//display:block</p>
            <ul class="menu1">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
            <p>//display:inline</p>
            <ul class="menu2">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
            <p>//display:inline-block</p>
            <ul class="menu3">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
            <p>//display:none</p>
            <ul class="menu4">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
            <p>//display:flex</p>
            <ul class="menu5">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
        </div>
        <div class="SubContent">
            <p>//よくある上部メニューを作成します。</p>
            <ul class="menu6">
                <li>商品紹介</li>
                <li>よくある質問</li>
                <li>会社概要</li>
                <li>お問い合わせ</li>
            </ul>
        </div>     
    </div>
</template>

<style scoped>
.MainContent{
    margin:5px;
    padding:20px;
}
.SubContent{
    margin:5px;
    padding:20px;
    border-top:solid;
}
.menu1 li{
    display:block;
    border:solid;
}
.menu2 li{
    display:inline;
    border:solid;
}
.menu3 li{
    display:inline-block;
    border:solid;
}
.menu4 li{
    display:none;
    border:solid;
}
.menu5{
    display:-webkit-flex;
    display:flex;
}
.menu5 li{
    border:solid;
}
.menu6 li{
    display:inline-block;
    margin:3px;
    padding:10px;
    background:#db7093;
    font-weight:bold;
    color:#ffffff;
    border-radius:5px;
    border-color:#ffffff;
}
.BorderBoxes{
    display:flex;
}
.BorderBox1{
    margin:5px;
    width:200px;
    height:200px;
    background: repeating-linear-gradient(45deg, #db7093, #db7093 10px, #088eb6 10px, #088eb6 20px);
}
.BorderBox2{
    margin:5px;
    width:200px;
    height:200px;
    background:repeating-linear-gradient(90deg, #db7093, #db7093 10px, #088eb6 10px, #088eb6 20px)
}
.BorderBox3{
    margin:5px;
    width:200px;
    height:200px;
    background:repeating-linear-gradient(0deg, #db7093, #db7093 10px, #088eb6 10px, #088eb6 20px)
}
.BorderBox4{
    margin:5px;
    width:200px;
    height:200px;
    background:repeating-linear-gradient(135deg, #db7093, #db7093 10px, #088eb6 10px, #088eb6 20px)
}
.BorderBox5{
    margin:5px;
    width:200px;
    height:200px;
    background:repeating-linear-gradient(135deg, #db7093, #db7093 20px, #088eb6 20px, #088eb6 40px)
}
.giji1{
    border:solid;
    width: 200px;
    display:flex;
}
.giji1:before{
    content:"★";
    position: absolute;
    left: -1px;
}
.giji2{
    border:solid;
    width:200px;
}
.giji2:after{
    content:"★";
    position: absolute;
    right: -1px;
}
</style>