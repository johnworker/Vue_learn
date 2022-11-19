<script>
export default {
  data() {
    return {
        // 傳回文字: ''(它的''是自定義輸出字樣的寫法)
      text: ''
    }
  },
  methods: {
    /* 輸入(變數){
        這個文字 = 變數.目標.值
    }*/
    onInput(e) {
      this.text = e.target.value
    }
  }
}
</script>

<template>
<!-- 使用v-bindandv-on一起，我們可以在表單輸入元素上創建(輸入和輸出)雙向綁定： -->
  <input :value="text" @input="onInput" placeholder="Type here">
  <p>{{ text }}</p>
</template>