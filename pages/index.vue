<template>
  <div class="container">
    <h1 class="title">freespace</h1>
    <div class="content">
      <v-btn small nuxt-link to="/reverselookup">Vueでやりたいこと逆引き</v-btn>
    </div>
    <div class="content">
      <div class="day">
        <p>201809</p>
        <v-btn small nuxt-link to="/day/2018/09/16">20180916</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/15">20180915</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/13">20180913</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/12">20180912</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/11">20180911</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/10">20180910</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/09">20180909</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/08">20180908</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/07">20180907</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/06">20180906</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/05">20180905</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/04">20180904</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/03">20180903</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/02">20180902</v-btn>
        <v-btn small nuxt-link to="/day/2018/09/01">20180901</v-btn>
      </div>
      <div class="day">
        <p>201808</p>
        <v-btn small nuxt-link to="/day/2018/08/31">20180831</v-btn>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container{
  margin:20px;
  padding-top: 10px;
}
.content{
  margin-top: 10px;
  padding:5px;
}
.title{
  color:#202020;
}
.day{
  margin-top:10px;
}
.day p{
  font-size:13px;
}
</style>