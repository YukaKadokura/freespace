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
</style>