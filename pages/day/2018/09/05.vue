<template>
    <div class="MainContent">
        <h1>20180905</h1>
        <div class="SubContent">
            <p>//テンプレートリテラルの検証です。</p>
            <p>//babelがきいてなくてできていない。</p>
            <p>{{ testForTemplateLiteral() }}</p>
        </div>
        <div class="SubContent">
            <p>//コールバック関数の検証です。</p>
            <p>{{ testForCallBack() }}</p>
        </div>
        <div class="SubContent">
            <p>//配列のdestructuring assignmentの検証です。</p>
            <p>//配列の一番最初の要素を返却します。</p>
            <p>{{ testForDestructuringAssignment() }}</p>
        </div>
        <div class="SubContent">
            <p>//LINE風吹き出しです。</p>
            <p>//わざと部品の一部を透明にしていません。</p>
            <div id="Balloon">
                <p>ふきだし</p>
            </div>
        </div>
        <div class="SubContent">
            <p>//display:inline; でリストの要素を横並びにします。</p>
            <ul id="menu1">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
        </div>
        <div class="SubContent">
            <p>//display:inline-block; でwidthを指定したリストの要素を横並びにします。</p>
            <ul id="menu2">
                <li>リスト1</li>
                <li>リスト2</li>
                <li>リスト3</li>
                <li>リスト4</li>
                <li>リスト5</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default{
    methods:{
        testForTemplateLiteral(){
            const NAME = '田中太郎';
            console.log('私の名前は${NAME}です。');
            return '私の名前は${NAME}です。';
        },
        testForCallBack(){
            function call(callback){
                console.log("受け取る方#call()");
                callback();
            }

            //引数に渡される関数がコールバック関数
            var reseivedFunc = function(){
                console.log("受け取られる方#reseivedFunc()");
            }

            //実行
            call(reseivedFunc);
        },
        testForDestructuringAssignment(){
            //配列の最初の要素だけを返す関数の宣言
            const head = ([x]) => x;
            //配列の宣言と結果の返却
            return head(['あいうえお', 'かきくけこ', 'さしすせそ']);
        }
    }
}
</script>

<style scoped>
.MainContent{
    padding:20ox;
    margin:5px;
}
.SubContent{
    padding:20px;
    margin:5px;
    border:dotted;
}
#Balloon{
    /* 配置方法が相対位置 */
    position: relative;

    /* 要素が生成するボックスの表示形式を横並びにする */
    display: inline-block;

    /* ボックスの幅 */
    margin: 15px;
	padding: 10px;
	min-width: 200px;
 	max-width: 100%;

    /* 色、文字 */
    color: #000000;
	font-size: 16px;
    background: #1dcd00;
    border-radius: 5px;
}

/* 選択した要素の最初の子要素として擬似要素を作成する */
#Balloon:before{
    content: "";

    /* 配置方法が絶対位置 */
    position: absolute;

    /* 上からの配置位置の指定 */
    top: 50%;

    /* 左からの配置位置の指定 */
    left: -30px;
    margin-top: -15px;

    /* わざと部品に使用するボーダーの色を透明にしない */
    border: 15px solid;
    border-right: 30px solid #1dcd00;
}
#menu1 li{
    margin: 5px;
    padding: 5px;
    display: inline;
    border: solid;
}
#menu2 li{
    margin: 5px;
    display: inline-block;
    width: 100px;
    text-align: center;
    border: solid;
}
</style>