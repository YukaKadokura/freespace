<template>
    <div class="content">
        <div class="header">
            <div class="side">
            <label class="toggle" for="open">
                MENU
            </label>
            <input id="open" type="checkbox">
            <div id="menu">
            <nav>
                <ul>
                <li><a href="#">トップページ</a></li>
                <li><a href="#">日々の記録</a></li>
                <li><a href="#">Vue逆引き</a></li>
                </ul>
            </nav>
            </div>
        </div>
        </div>
        <h1 id="title">20180908</h1>
        <div class="main">
            <div class="sub">
                <p>//文字の横ラインを揃えます。</p>
                <div class="flex">
                    <div>
                        <p>//top</p>
                        <span class="oya">あ<span class="top">いうえお</span></span>
                    </div>
                    <div>
                        <p>//text-top</p>
                        <span class="oya">あ<span class="texttop">いうえお</span></span>
                    </div>
                    <div>
                        <p>//middle</p>
                        <span class="oya">か<span class="middle">きくけこ</span></span>
                    </div>
                    <div>
                        <p>//bottom</p>
                        <span class="oya">さ<span class="bottom">しすせそ</span></span>
                    </div>
                    <div>
                        <p>//baseline</p>
                        <span class="oya">た<span class="baseline">ちつてと</span></span>
                    </div>
                </div>
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
}
.header{
    background:crimson;
    height:80px;
    margin:0;
    padding:10px;
}
#title{
    padding:10px;
    color:white;
}
.content{
    background:tomato;
    height:100%;
    color:white;
}
.side{
    margin:20px;
}
ul {
  margin: 0;
  padding-left: 0;
}
 
li {
  list-style:none;
  font-weight:bold;
  padding:5px;
}
 
a {
  text-decoration:none;
  color:white;
}
 
#menu {
  position: fixed;
  top: 0;
  right: -190px; /* メニューのwidth + padding */
  width: 150px; /* メニューのwidth */
  height: 100%;
  padding: 20px;
  transition: left .5s, right .5s; /* アニメーション */
  background-color: rgba(86, 86, 86, .7);
}
 
.toggle {
  font-size: 20px;
  cursor: pointer;
  font-weight:bold;
  border:solid;
  padding:5px;
}
 
.toggle:hover {
  text-decoration: underline;
}
 
#open {
  display: none;
}
 
/* :checked 擬似クラスを使って、#openがチェック状態になった時に、#menuが「right: 0;」になります。 */
#open:checked + #menu {
  right: 0;
}

.main{
    margin:5px;
    padding:5px;
}

.sub{
    margin:5px;
    padding:5px;
}

.flex{
    display:flex;
}

.flex div{
    margin:5px;
}

.oya{
    font-size:50px;
}

.top{
    font-size:15px;
    vertical-align:top;
}

.texttop{
    font-size:15px;
    vertical-align:text-top;
}

.middle{
    font-size:15px;
    vertical-align:middle;
}

.bottom{
    font-size:15px;
    vertical-align:bottom;
}

.baseline{
    font-size:15px;
    vertical-align:baseline;
}

</style>