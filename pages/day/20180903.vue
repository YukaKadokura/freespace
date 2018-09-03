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
                <button class="button-test" v-bind:disabled="vbindtest">v-bindによるボタンの非活性</button>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            vbindtest : false
        }
    }
}
</script>

<style>
.MainContent{
    padding: 20px;
}
.SubContent{
    margin: 5px;
    padding: 20px;
    border: solid;
}
.button-test{
    margin: 10px;
    padding: 15px;
    border-radious: 5px;
    -webkit-border-radius: 5px;/* for Safari and Chrome 対応*/
    -moz-border-radius: 5px;/* for Firefox 対応*/
    color: #ffffff;
    background-color: #ff0000;
}
</style>