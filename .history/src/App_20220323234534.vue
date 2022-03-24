<template>
  <div id="app">
    {{ info }}
  </div>
</template>

<script>
export default {
  methods: {
    run() {
      let result;
      console.log("同期処理終了");
      result = "完了";
      const message = "同期処理";
      console.log(message + result);
    },
  },
  created() {
    this.run();
  },
};
</script>
