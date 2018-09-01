<template>
    <div id="MainContent">
        <h1>20180901</h1>
        <div class="SubContent">
            <p>//最初からテキストフィールドに文字が入っていて、入力した内容的が下に表示される。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="userInputData" label="文字を入力してください"></v-text-field>
            </v-flex>
            <p>入力した文字：{{ userInputData }}</p>
        </div>
        <div class="SubContent">
            <p>//入力した文字を、用意されていた文字列と結合して表示させる。未入力の場合は表示しない。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="userInputData2" label="文字を入力してください"></v-text-field>
            </v-flex>
            <p>{{ getUserInputData2() }}</p>
        </div>
        <div class="SubContent">
            <p>//入力された10進数の整数を2真数に変換して表示する。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="num10" label="10進数を入力してください"></v-text-field>
            </v-flex>
            <v-btn v-on:click="convertToNum10()">変換</v-btn>
            <p>{{ error }}</p>
            <p>{{ num2 }}</p>
        </div>
        <div class="SubContent">
            <p>//NaNの判定をする</p>
            <p>Number.isNaN(0)：{{ test1() }}</p>
        </div>
        <div class="SubContent">
            <p>//入力された値が整数か判定する</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="inputStr"></v-text-field>
            </v-flex>
            <p>{{ isNumber() }}</p>
        </div>
    </div>
</template>

<script>
export default{
    head:{
        title:"20180901のページ"
    },
    asyncData(){
        return{
            userInputData : "alreacy input.",
            userInputData2 : "",
            num10 : "",
            num2 : "",
            error : "",
            inputStr : ""
        }
    },
    methods:{
        getUserInputData2(){
            if(this.userInputData2 != '' && this.userInputData2 != null){
                return "入力した文字は「" + this.userInputData2 + "」です。"
            }else{
                return "";
            }
        },
        convertToNum10(){
            if(this.num10 == ""){
                this.num2 = "";
                this.error = "入力されていません。";
                return;
            }
            
            var num = Number(this.num10);

            if(!(num >= 0)){
                this.num2 = "";
                this.error = "数値を入力してください。";
                return;
            }

            if(!Number.isInteger(num)){
                this.num2 = "";
                this.error = "小数ではなく整数を入力してください。"
                return;
            }

            var ans = 1;
            var amari = 0;
            var num2 = "";
            while(ans != 0){
                ans = parseInt(num / 2);
                amari = num % 2;
                num2 = num2 + String(amari);
                num = ans;
            }
            this.error = "";
            this.num2 = num2.split("").reverse().join("");
        },
        test1(){
            return Number.isNaN(0);
        },
        isNumber(){
            if(this.inputStr == ""){
                return "";
            }
            return Number.isInteger(Number(this.inputStr));
        }
    }
}
</script>

<style>
#MainContent{
    padding:20px;
}
.SubContent{
    margin:5px;
    padding:20px;
    border:solid;
}
</style>