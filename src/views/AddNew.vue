<template>
  <div class="addnew">
    <div class="container">
      <h1>Add new todo item</h1>
      <form @submit.prevent>
        <label for="desc">Description</label>
        <input type="text" name="desc" v-model="desc" />

        <label for="author">Author</label>
        <input type="text" name="author" v-model="author" />
        <router-link to="/"><button @click="addTodo">Add</button></router-link>
      </form>
      <img
        src="../assets/floddjungel.png"
        alt="A footer image of a jungle river."
        class="background"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      author: "",
      desc: "",
      date: new Date().toLocaleString("en-GB"),
      completed: false,
    };
  },

  methods: {
    addTodo: function () {
      this.$store.commit("addTodo", {
        author: this.author,
        desc: this.desc,
        date: this.date,
      });
    },
  },
};
</script>

<style>
form {
  width: 60%;
  margin: 0 auto;
}

input {
  display: block;
  width: 100%;
  height: 2rem;
  margin-bottom: 1rem;
}

.container {
  position: relative;
}

.background {
  position: absolute;
  bottom: 0;
  width: 100%;
  pointer-events: none;
}
</style>