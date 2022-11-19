<script>
export default {
  data() {
    return {
        // 目前資料回傳awesome為真
      awesome: true
    }
  },
  methods: {
    toggle() {
        // 用toggle觸發點擊事件切換awesome的真假
      this.awesome = !this.awesome
    }
  }
}
</script>

<template>
  <button @click="toggle">toggle</button>
  <!-- 僅當<h1>的值為真時awesome才會呈現。
    如果awesome更改為虛假值，它將從 DOM 中刪除。 -->
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>
</template>