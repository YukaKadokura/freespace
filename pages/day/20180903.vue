<template>
    <div class="MainContent">
        <div class="SubContent">
            <p>//v-bindディレクティブ</p>
            <p>//値的にnullまたはfalseまたはundefinedが入った場合はボタンが活性化します。（文字列ではない）</p>
                <v-flex xs12 sm6 md3>
                    <v-text-field v-model="vbindtest"/>
                </v-flex>
                <p>Mastacheによるバインド：{{ vbindtest }}</p>
                <button class="button-test">ただのボタン</button>
                <button class="button-test" v-bind:disabled="vbindtest">v-bindによるボタンの活性</button>
        </div>
        <div class="SubContent">
            <p>//LINE風の吹き出し（<a href="https://saruwakakun.com/html-css/reference/speech-bubble">参考</a>）</p>
            <div class="balloon">
                <p>吹き出し</p>
            </div>
        </div>
        <div class="SubContent">
            <p>//入力された2進数を10進数に変換して表示します。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="binaryNum" />
            </v-flex>
            <p>変換後の10進数：{{ decimalNumToBinaryNum() }}</p>
        </div>
        <div class="SubContent">
            <p>//入力された値が素数かチェックします。（ver1）</p>
            <v-flex xs12 sm6 md3>
                <v-text-field solo v-model="inputNum"/>
            </v-flex>
            <p>素数かどうか：{{ isPrimeNum() }}</p>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            vbindtest : false,
            binaryNum : "",
            inputNum: ""
        }
    },
    methods:{
        decimalNumToBinaryNum(){
            if(this.binaryNum == null || this.binaryNum == ""){
                return "入力されていません。";
            }
            var decimalNum = this.binaryNum.split("").reverse();
            var count = 0;
            for(var i=0; i<decimalNum.length; i++){
                if(decimalNum[i] != 0 && decimalNum[i] != 1){
                    return "2進数を入力してください";
                }
                if(decimalNum[i] == "0"){
                    continue;
                }
                var num = Number(decimalNum[i]);
                count = count + Math.pow(2, i);
            }
            return count;
        },
        isPrimeNum(){
            var input = Number(this.inputNum);
            if(!(input >= 1)){
                return "1以上の整数を入力して下さい。";
            }
            if(input != 2 && input%2 == 0){
                return "素数ではありません。";
            }

            var half = input/2;
            for(var i=2; i<half; i++){
                if(input%i == 0){
                    return "素数ではありません。"
                }
            }
            return "素数です。";
        }
    }
}
</script>

<style>
.MainContent{
    padding: 20px;
}
.SubContent{
    background-color: #f2f2f2;
    margin: 5px;
    padding: 20px;
    border: solid;
}
.button-test{
    margin: 10px;
    padding: 15px;
    border-radius: 5px;
    -webkit-border-radius: 5px;/* for Safari and Chrome 対応*/
    -moz-border-radius: 5px;/* for Firefox 対応*/
    color: #ffffff;
    background-color: #ff0000;
}
.balloon {
 	position: relative;
	display: inline-block;
 	margin: 15px;
	padding: 10px;
	min-width: 200px;
 	max-width: 100%;
 	color: #000000;
	font-size: 16px;
	background: #1dcd00;
    border-radius: 5px;
}
.balloon:before{
	content: "";
	position: absolute;
	top: 50%;
	left: -30px;
 	margin-top: -15px;
	border: 15px solid transparent;
	border-right: 30px solid #1dcd00;
}
</style>