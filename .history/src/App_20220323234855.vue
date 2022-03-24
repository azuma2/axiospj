<template>
  <div id="app">
    {{ info }}
  </div>
</template>

<script>
import axios from "axios";
export default {
  methods: {
    run() {
      let result;
      axios
        .get("https://api.coindesk.com/v1/bpi/currentprice.json")
        .then(() => {
          //非同期処理終了時に実行されるメソッド
          console.log("非同期処理終了");
          result = "完了";
          const message = "非同期処理";
          console.log(message + result);
        });
    },
  },
  created() {
    this.run();
  },
};
</script>
