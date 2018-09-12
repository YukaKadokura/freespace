<template>
    <div>
        <h1>{{ title }}</h1>
        <div class="grid">
            <div class="item1">
                アイテム1
            </div>
            <div class="item2">
                アイテム2
            </div>
            <div class="item3">
                アイテム3
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180912"
        }
    }
}
</script>

<style>
.grid{
    display:grid;
    grid-template-rows: 200px 200px 200px;
    grid-template-columns: 200px 200px 200px;
}
.item1{
    background:red;
    width:100px;
    height:100px;
    grid-row: 1 / 3;
    grid-column: 1 / 3;
}
.item2{
    background:blue;
    width:100px;
    height:100px;
    grid-row: 2 / 3;
    grid-column: 2 / 3;
}
.item3{
    background:yellow;
    width:100px;
    height:100px;
    grid-row: 3/ 3;
    grid-column: 3/ 3;
}
</style>