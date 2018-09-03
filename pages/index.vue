<template>
  <div class="MainContent">
    <h1>freespace</h1>
    <div class="Contents">
      <v-btn small nuxt-link to="/reverselookup">Vueでやりたいこと逆引き</v-btn>
    </div>
    <div class="Contents">
      <v-btn small nuxt-link to="/day_20180903">20180903</v-btn>
      <v-btn small nuxt-link to="/day/20180902">20180902</v-btn>
      <v-btn small nuxt-link to="/day/20180901">20180901</v-btn>
      <v-btn small nuxt-link to="/day/20180831">20180831</v-btn>
    </div>
  </div>
</template>

<style>
.MainContent{
  padding: 20px;
}
.Contents{
  margin: 5px;
}
</style>