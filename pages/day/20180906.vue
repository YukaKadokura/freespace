<template>
    <div class="MainContent">
        <h1>20180906</h1>
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
        </div>
        <div class="SubContent">
            <p>//よくある上部メニューを作成します。</p>
            <ul class="menu5">
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
    border-bottom:solid;
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
.menu5 li{
    display:inline-block;
    margin:3px;
    padding:10px;
    background:#db7093;
    font-weight:bold;
    color:#ffffff;
    border-radius:5px;
    border-color:#ffffff;
}
</style>