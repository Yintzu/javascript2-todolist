<template>
  <div class="home">
    <div class="container">
      <h1>Welcome to your todo list</h1>
      <TodoList />
    </div>
  </div>
</template>

<script>
import TodoList from "../components/TodoList";

export default {
  name: "Home",
  components: {
    TodoList,
  },
};
</script>