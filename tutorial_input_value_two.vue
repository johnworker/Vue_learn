<script>
export default {
  data() {
    return {
      text: ''
    }
  }
}
</script>

<template>
<!-- v-model自動將 "" 的值與綁定狀態同步<input>，因此我們不再需要為此使用事件處理程序。 -->
  <input v-model="text" placeholder="Type here">
  <p>{{ text }}</p>
</template>

v-model不僅適用於文本輸入，還適用於其他輸入類型，例如復選框、單選按鈕和選擇下拉菜單。

我們在Guide-Form Bindings中介紹了更多細節。
