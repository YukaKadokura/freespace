<template>
    <div class="MainContent">
        <h1>20180904</h1>
        <div class="SubContent NoNewLine">
            <p>//Mastache内でJSの式がかけることの検証です。<p>
            <p>//かつ、v-layoutとv-flexの検証です。</p>
            <v-container>
                <v-layout align-center justify-start row fill-height>
                    <v-flex xs1 sm1 md1>
                        <v-text-field v-model="inMastache" />
                    </v-flex>
                    <v-flex>
                        + 1 = <span>{{ Number(inMastache) + 1 }}</span>
                    </v-flex>
                </v-layout>
            </v-container>
        </div>
        <div class="SubContent">
            <p>//v-ifの検証です。</p>
            <p v-if="seen">この行は、バインドされた値がtrueなら表示されます。</p>
        </div>
        <div class="SubContent">
            <p>//CSSで文字列の折り返しをさせない検証です。</p>
            <p>//white-space:nowrapを使用します。</p>
            <div class="Return UseReturn">
                <span>文字の折り返しあり文字の折り返しあり文字の折り返しあり文字の折り返しあり文字の折り返しあり</span>
            </div>
            <div class="Return NoReturn">
                <span>文字の折り返しなし文字の折り返しなし文字の折り返しなし文字の折り返しなし文字の折り返しなし</span>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            inMastache: "1",
            seen: true
        }
    }
}
</script>

<style scoped>
.MainContent{
    padding: 20px;
}
.SubContent{
    margin: 5px;
    padding: 20px;
    border: solid;
}
.Return{
    padding: 20px;
    margin: 5px;
    width: 30%;
    border: solid;
}
.NoReturn{
    white-space: nowrap;
}
</style>