<script>
export default {
  data() {
    return {
      titleClass: 'title'
    }
  }
}
</script>

<template>
<!-- ( :class) 冒號之後的部分是指令的“參數”。
在這裡，元素的class屬性將與titleClass組件狀態中的屬性同步。 -->

  <h1 :class="titleClass">Make me red</h1>
</template>

<style>
/* 設定樣式 */
.title {
  color: red;
}
</style>

說明：

指令是一個以v-前綴開頭的特殊屬性。
它們是 Vue 模板語法的一部分。
與文本插值類似，指令值是可以訪問組件狀態的 JavaScript 表達式。
Guide-Template Syntaxv-bind中討論了指令語法的全部細節。