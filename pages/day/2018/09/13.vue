<template>
    <div>
        <h1>{{ title }}</h1>
        <div class="circle">
        まる
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            title:"20180913"
        }
    }
}
</script>

<style scoped>
.circle{
    width:100px;
    height:100px;
    padding:30px;
    border-radius:50%;
    background:skyblue;
}
</style>