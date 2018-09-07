<template>
    <div class="content">
        <h1 id="title">20180908</h1>
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
        <div class="main">
            <div class="sub">
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
#title{
    padding:20px;
    color:white;
}
.content{
    background:tomato;
    height:100%;
}
.side{
    margin:20px;
}
ul {
  margin: 0;
  padding-left: 0;
}
 
li {
  list-style: none;
  padding:5px;
}
 
a {
  text-decoration: none;
  color: #fff;
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
  font-size: 30px;
  cursor: pointer;
  color:white;
  font-weight:bold;
  border:solid;
  padding:5px;
  margin:10px;
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
    margin:20px;
    padding:5px;
}

.sub{
    margin:5px;
    padding:5px;
}
</style>