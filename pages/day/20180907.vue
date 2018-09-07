<template>
    <div class="content flex">
        <div class="menu">
            <ul>
                <li>トップページ</li>
                <li>日々の記録</li>
                <li>Vue逆引き</li>
            </ul>
        </div>
        <div class="MainContent">
            <p class="pankuzu">トップページ > 日々の記録 > 20180907</p>
            <h1>20180907</h1>
            <div class="SubContent">
                <p>//CSSで丸を作ります。</p>
                <div class="circles flex">
                    <div class="circle circle1">
                        円です。
                    </div>
                    <div class="circle circle2">
                        文字を中央に寄せた円です。
                    </div>
                    <div class="circle circle3">
                        枠線の円です。
                    </div>
                </div>
            </div>
            <div class="SubContent">
                <p>//文字を縦書きにします。</p>
                <div class="flex">
                    <p class="vertical">あいうえお</p>
                    <p class="vertical">かきくけこ</p>
                    <p class="vertical">さしすせそ</p>
                </div>
            </div>
            <div class="SubContent">
                <p>//HTMLのdetails、summary要素の検証です。</p>
                <details>
                    <summary>
                        概要はsummaryタグで囲い、summaryタグをdetailsタグで囲みます。
                    </summary>
                    詳細な内容はsummaryタグで囲まないdetailsタグの内部に書きます。
                </details>
            </div>
        </div>
    </div>
</template>

<style scoped>
html{
    height:100%;
}
body{
    height:100%;
    margin:0;
}
.content{
    background:#bc8f8f;
}
.menu{
    margin:0;
    background:#48d1cc;
}
.menu li{
    font-weight:bold;
    color:#ffffff;
    border: none;

    display:block;
    padding:15px 30px 15px 15px;
    list-style:none;
}
.MainContent{
    margin:20px;
    padding:20px;
    background:#ff0000;
}
.pankuzu{
    font-size:11px;
}
.SubContent{
    margin:5px;
    padding:20px;
    border-top:solid;
}
.flex{
    display:flex;
    height:100%;
    width:100%;
}
.circle{
    margin:5px;
}
.circle1{
    width:200px;
    height:200px;
    background:#c71585;
    border-radius:50%
}
.circle2{
    width:200px;
    height:200px;
    background:#008b8b;
    border-radius:50%;
    
    /*テキスト中央寄せ*/
    text-align:center;
    vertial-align:middle;
    padding:60px;
}
.circle3{
    width:200px;
    height:200px;
    border-radius:50%;
    border:solid 5px #6495ed;
    background:#ffffff;
    padding:50px;
    text-align:center;
}
.vertical{
    -webkit-writing-mode:vertical-rl;
    -ms-writing-mode:rb-rl;
    writing-mode:vertical-rl;
}
</style>