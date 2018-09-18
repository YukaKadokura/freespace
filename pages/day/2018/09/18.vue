<template>
    <div class="contents">
        <h1>{{ title }}</h1>
        <div class="content c1">
            <h2>よくあるカラム</h2>
            <div>
                <header>
                    <div class="box">header</div>
                </header>
                <main>
                    <div class="box">
                        <div id="left">左</div>
                        <div id="right">右</div>
                    </div>
                    <div style="clear:both;"></div>
                </main>
                <footer>
                    <div class="box">footer</div>
                </footer>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180918"
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
    margin-top:5px;
}
.content h2{
    font-size:20px;
    padding:5px;
    border-bottom:dashed 1px #454545;
    width:50%;
    margin-bottom:5px;
}
.box{
    width:500px;
    margin: 0 auto;
}
header{
    background:tomato;
}
main{
    background:skublue;
}
footer{
    clear:both;
    background:slategray;
}
#left{
    background:limegreen;
    float:left;
    width:200px;
}
#right{
    background:lightgreen;
    float:left;
    width:300px;
}
</style>