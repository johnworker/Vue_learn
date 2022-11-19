// 點擊次數蝶家監聽事件

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
    // 方法
  methods: {
    // increment 加法函式
    increment() {
      this.count++
    }
  }
}
</script>

<template>
<!-- v-on我們可以使用指令監聽 DOM 事件：(原始寫法)
    <button v-on:click="increment">{{ count }}</button>
 -->

 <!-- 由於它的頻繁使用，v-on也有一個簡寫語法：
    <button @click="increment">{{ count }}</button>
 -->

<!-- 運作方式：按鈕點擊加法函式後增加計數 -->
  <button @click="increment">count is: {{ count }}</button>
</template>
