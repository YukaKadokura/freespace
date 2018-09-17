<template>
    <div class="contents">
        <h1>{{ title }}</h1>
        <div class="content c1">
            <h2>おみくじ</h2>
            <div id="omikuji" v-on:click="getOmikujiResult()" v-on:mousedown="mousedownOmikuji()" v-on:mouseup="mouseupOmikuji()">
                {{ omikujiResult }}
            </div>
        </div>
        <div class="content c2">
            <h2>5秒を当てるゲームです。</h2>
            <div class="fivegame">
                <div id="target">5.000</div>
                <div id="result">{{ resultTime }}</div>
                <div class="buttons">
                    <div id="start" v-on:click="gameStart()">Start</div>
                    <div id="stop" v-on:click="gameStop()">Stop</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180917",
            omikujiResult:"？",
            startTime:"",
            resultTime:""
        }
    },
    methods:{
        getOmikujiResult(){
            var results = [ "凶", "吉", "中吉", "大吉" ];
            var num = Math.floor(Math.random() * 4);
            this.omikujiResult = results[num];
        },
        mousedownOmikuji(){
            (() => {
                var omikuji = document.getElementById('omikuji');
                omikuji.classList.add('pushed');
            })();
        },
        mouseupOmikuji(){
            (() => {
                var omikuji = document.getElementById('omikuji');
                omikuji.classList.remove('pushed');
            })();
        },
        gameStart(){
            this.startTime = Date.now();
            this.resultTime = "計測中";
        },
        gameStop(){
            this.resultTime = (Date.now() - new Date(this.startTime))/1000;
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
.content h2{
    margin:10px 0 10px 0;
    font-size:15px;
    color:#454545;
    padding:5px;
    border-left:solid 3px #454545;
}
#omikuji{
    width:200px;
    height:200px;
    border-radius:50%;
    background:red;
    text-align:center;
    padding:40px;
    color:white;
    font-weight:bold;
    font-size:30px;
    cursor: pointer;
    opacity: 0.9;
    box-shadow: 0 10px 0 #D1483E;
    border:3px solid #D1483E;
    user-select: none;
}
#omikuji:hover{
    opacity:1;
}
.pushed{
    background:yellow;
    height:190px;
    box-shadow: 0 4px 0 #D1483E;
}
.fivegame{
    font-family: 'Courier New', sans-serif;
    width:300px;
    text-align:center;
    font-weight:bold;
}
#target, #result{
    font-size:32px;
    margin-bottom:15px;
    background:#ccc;
    height:60px;
    line-height:60px;
}
#start{
    float:left;
}
#stop{
    float:right;
} 
#start, #stop{
    cursor:pointer;
    font-size:18px;
    width:145px;
    background:#eee;

    height:40px;
    line-height:40px;
    box-shadow:0 6px 0 #ccc;
}
</style>