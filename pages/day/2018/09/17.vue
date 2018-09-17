<template>
    <div class="contents">
        <h1>{{ title }}</h1>
        <div class="content c1">
            <h2>おみくじ</h2>
            <div id="omikuji" v-on:click="getOmikujiResult()" v-on:mousedown="mousedownOmikuji()" v-on:mouseup="mouseupOmikuji()">
                {{ omikujiResult }}
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180917",
            omikujiResult:"？"
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
                'use strict';
                var omikuji = document.getElementById('omikuji');
                omikuji.classList.add('pushed');
            })();
        },
        mouseupOmikuji(){
            (() => {
                'use strict';
                var omikuji = document.getElementById('omikuji');
                omikuji.classList.remove('pushed');
            })();
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
#omikuji{
    margin:30px 0 0;
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
</style>