<script>
// give each todo a unique id
let id = 0;

export default {
  data() {
    return {
      newTodo: "",
      todos: [
        { id: id++, text: "Learn HTML" },
        { id: id++, text: "Learn JavaScript" },
        { id: id++, text: "Learn Vue" },
      ],
    };
  },
  methods: {
    addTodo() {
      this.todos.push({ id: id++, text: this.newTodo });
      this.newTodo = "";
    },
    removeTodo(todo) {
      this.todos = this.todos.filter((t) => t !== todo);
    },
  },
};
/* 輸出預設值 {
    資料() {
        回傳 {
            新執行: '',    
                執行: [
                    {編號: 編號遞增, 文字: '字串'},
                    {編號: 編號遞增, 文字: '字串'},
                    {編號: 編號遞增, 文字: '字串'}
                ],
            };
        },
    方法: {
       增加執行() {
        這個.執行(s).推送({ 編號: 編號遞增, 文字: 這個.新執行 });
        這個.新執行 = "";
    },
    移除執行(執行) {
      這個.執行(s) = 這個.執行(s).篩選((t) => t !== todo);
    },
  },
    };
        */
</script>

<template>
  <!-- 表單送出鈕 -->
  <form @submit.prevent="addTodo">
    <!-- 輸入框 -->
    <input v-model="newTodo" />
    <!-- 按鈕 -->
    <button>Add Todo</button>
  </form>
  <!-- 選單輸出 -->
  <ul>
    <!-- 列表迴圈 -->
    <li v-for="todo in todos" :key="todo.id">
      <!-- 輸出文字 -->
      {{ todo.text }}
      <!-- 按鈕 -->
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>