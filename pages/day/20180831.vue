<template>
    <div id="content">
        <h1>20180831</h1>
        <div id="content1">
          <p>//送信ボタンを押すとアラートが出る</p>
          <v-btn small v-on:click="onSubmitted('送信')">送信ボタン</v-btn>
        </div>
        <div id="content2">
          <p>//テキストフィールドに入力すると入力した文字列が下に表示され、そのままボタンを押すとアラート内に入力した文字列が表示される</p>
          <v-flex xs12 sm6 md3>
            <v-text-field v-model="name" label="名前は？"></v-text-field>
            <p>Your name： {{ name }} </p>
            <v-btn v-on:click="getText()">テキストの送信</v-btn>
          </v-flex>
        </div>
    </div>
</template>

<script>
export default {
  head: {
    title: '20180831のページ'
  },
  asyncData() {
    return {
      name: ""
    }
  },
  methods: {
    onSubmitted(message) {
      alert('onSubmitted!：' + message);
    },
    getText(){
      alert('you inputed!：' + this.name);
    },
  }
}
</script>

<style>
#content{
  padding: 20px;
  
}
#content1{
  margin: 5px;
  padding: 20px;
  border: solid;
}
#content2{
  margin: 5px;
  padding: 20px;
  border: solid;
}
</style>