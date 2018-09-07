<template>
    <div class="Content">
        <h1>20180902</h1>
        <div class="SubContent">
            <p>//Web記事の見出しに使用可能な見出しタブです。</p>
            <v-flex xs12 sm6 md3>
                <div id="midashi">
                    <h2>見出しの内容</h2>
                </div>
            </v-flex>
        </div>
        <div class="SubContent">
            <p>//data()メソッドを使用してバインドします。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="bind1" />
                <p>入力した文字：{{ bind1 }}</p>
            </v-flex>
        </div>
        <div class="SubContent">
            <p>//asyncData()メソッドを使用してバインドします。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="bind2" />
                <p>入力された文字：{{ bind2 }}</p>
            </v-flex>
        </div>
        <div class="SubContent">
            <p>//data()にはbind3に"data()"、asyncData()には"asyncData()"をセットしておきます（どちらで上書きされるか確認）。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="bind3" />
                <p>入力した文字：{{ bind3 }}</p>
            </v-flex>
        </div>
        <div class="SubContent">
            <p>//v-onceの検証です。</p>
            <p>//データ変更時の更新はおこなわず、一度だけ展開することができます。</p>
            <v-flex xs12 sm6 md3>
                <v-text-field v-model="bind4" />
                <p>入力した文字：{{ bind4 }}</p>
                <p v-once>初期値：{{ bind4 }}</p>
            </v-flex>
        </div>
        <div class="SubContent">
            <p>//v-htmlの検証です。</p>
            <p>//2重中括弧のmustachesは、データをHTMLではなく、プレーンなテキストとして扱います。</p>
            <p>//実際の HTML として出力するためには、v-html ディレクティブを使用する必要があります</p>
            <p>文字：{{ rowHTML }}</p>
            <p>HTMLとして解釈：<span v-html="rowHTML"></span></p>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            bind1 : "",
            bind3 : "data()",
            bind4 : "これは初期値です",
            rowHTML : "<b>太字になればHTMLとして解釈されていることになる</b>"
        }
    },
    asyncData(){
        return{
            bind2 : "",
            bind3 : "asyncData()"
        }
    }
}
</script>

<style scoped>
.Content{
    padding:20px;
}
.SubContent{
    margin:5px;
    padding:20px;
    border:solid;
}
#midashi{ /*見出し本体*/
    position: relative;
    color: black;
    background: #d0ecff;
    line-height: 1.4;
    padding: 0.25em 0.5em;
    margin: 2em 0 0.5em;
    border-radius: 0 5px 5px 5px;
}
#midashi:after { /*タブ*/
    position: absolute;
    font-family: "Font Awesome 5 Free",'Quicksand','Avenir','Arial',sans-serif;
    content: 'タブのタイトル';
    background: #2196F3;
    color: #fff;
    left: 0px;
    bottom: 100%;
    border-radius: 5px 5px 0 0;
    padding: 3px 7px 1px;
    font-size: 0.7em;
    line-height: 1;
    letter-spacing: 0.05em
}

</style>