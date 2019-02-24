<template>
  <div>
    <BaseInputText v-model="newToolText" @keydown.enter="addTodo"/>
    <ul v-if="todos.length">
      <TodoListItem v-for="todo in todos" :key="todo.id" :todo="todo" @remove="removeTodo"/>
    </ul>
  </div>
</template>
<script>
import BaseInputText from "./BaseInputText.vue";
import TodoListItem from "./TodoListItem.vue";
let nextTodoId = 1;
export default {
  components: {
    BaseInputText,
    TodoListItem
  },
  data: function() {
    return {
      newToolText: "",
      todos: [
        { id: nextTodoId++, text: "Learn" },
        { id: nextTodoId++, text: "vue" }
      ]
    };
  },
  methods: {
    addTodo(e) {
      const text = this.newToolText.trim();
      if (text) {
        this.todos.push({
          id: nextTodoId++,
          text: text
        });
      }
    },
    removeTodo(e) {
      this.todos = this.todos.filter(todo => {
        return todo.id !== e;
      });
    }
  }
};
</script>
<style scoped>
div {
  
}
</style>
