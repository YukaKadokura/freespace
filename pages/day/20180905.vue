<template>
    <div class="MainContent">
        <h1>20180905</h1>
        <div class="SubContent">
            <p>//テンプレートリテラルの検証です。</p>
            <p>//babelがきいてなくてできていない。</p>
            {{ testForTemplateLiteral() }}
        </div>
    </div>
</template>

<script>
export default{
    methods:{
        testForTemplateLiteral(){
            //テンプレートリテラルの検証
            const NAME = "田中太郎";
            console.log('私の名前は${NAME}です。');
            return '私の名前は${NAME}です。';
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