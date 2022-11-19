<script>
// export default 導出預設值
export default {
  data() {
    /* 回傳 {
      訊息: 'Hello World!',
      計數器: {
        計數: 0
        },
      };*/
    return {
      message: "Hello World!",
      counter: {
        count: 0,
      },
    };
  },
};
</script>

<template>
  <!-- 在h1的地方呼叫message 用{{ message }} -->
  <h1>{{ message }}</h1>

  <!-- 在p的地方呼叫 計數 用{{ counter.count }} -->
  <p>Count is: {{ counter.count }}</p>

<!-- 在h2的地方呼叫message的倒敘輸出 用{{ message.split('').reverse().join('') }} -->
  <h2>{{ message.split('').reverse().join('') }}</h2>

</template>