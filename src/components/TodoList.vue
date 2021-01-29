<template>
  <div class="TodoList">
    <TodoItem v-for="(todo, i) in todolist" :key="i" :todo="todo" />
    <p v-if="this.$store.state.todolist.length === 0">No todos :(</p>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  components: {
    TodoItem,
  },

  computed: {
    todolist() {
      return this.$store.state.todolist;
    },
  },
};
</script>

<style scoped>
.TodoList {
  margin: 0 auto;
  padding: 2rem;
  background: rgb(220, 255, 220);
  width: 80%;
  text-align: center;
  box-shadow: 0px 0px 5px;
}
</style>