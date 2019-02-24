<template>
  <div id="app">
    <h1>To-Do-List</h1>
    <TodoList></TodoList>
  </div>
</template>

<script>
import TodoList from "./components/TodoList.vue";
export default {
  components: {
    TodoList
  }
};
</script>

<style >
#app {
  padding: 0;
  margin: 0 auto;
  max-width: 400px;
}
#app h1 {
  text-align: center;
  font-size: 48px;
  font-weight: 200;
}
</style>
