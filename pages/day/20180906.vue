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
</style>