<template>
  <div class="TodoItem" :class="{ completed: this.todo.completed }">
    <div class="grid">
      <div class="col1">
        <div class="flexer">
          <p class="desc">{{ todo.desc }}</p>
          <p>{{ todo.date }}</p>
        </div>
        <div class="flexer">
          <p>{{ todo.author }}</p>
          <div class="buttons">
            <button @click="completeTodo">Completed</button>
            <button @click="removeTodo">Remove</button>
          </div>
        </div>
      </div>
      <div class="col2">
        <button class="up" @click="moveTodoUp">↑</button>
        <button class="down" @click="moveTodoDown">↓</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["todo"],
  methods: {
    removeTodo() {
      this.$store.commit("removeTodo", this.todo);
    },
    completeTodo() {
      this.$store.commit("completeTodo", this.todo);
    },
    moveTodoUp() {
      this.$store.commit("moveTodoUp", this.todo);
    },
    moveTodoDown() {
      this.$store.commit("moveTodoDown", this.todo);
    },
  },
};
</script>

<style scoped>
.TodoItem {
  border: 1px solid black;
  width: 100%;
  min-height: 50px;
  margin: 1rem auto 1rem auto;
  background: white;
}

.completed {
  background: lightgrey;
}

.desc {
  font-size: 1.2rem;
  font-weight: 600;
  margin: 0;
}

.grid {
  display: grid;
  grid-template-columns: 95% 5%;
}

.col2 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.flexer {
  display: flex;
  justify-content: space-between;
}

.flexer p {
  margin: 0.5rem 1rem 0.5rem 1rem;
}

.buttons button {
  margin: 0 1rem 0.5rem 0;
}

.col2 button {
  display: block;
  margin: 0;
}

button.down {
  margin-top: 3px;
}
</style>