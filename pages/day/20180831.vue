<template>
    <div>
        <h1>20180831</h1>
        <div>
            <p>//送信ボタンを押すとアラートが出る</p>
            <v-btn small v-on:click="onSubmitted('送信')">送信ボタン</v-btn>
        </div>
    </div>
</template>

<script>
export default {
  methods: {
    onSubmitted(message) {
      alert('onSubmitted!：' + message);
    },
  },
}
</script>