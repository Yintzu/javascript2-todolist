<template>
  <div id="app">
    <div id="nav">
      <NavBar />
    </div>
    <router-view />
  </div>
</template>

<script>
import NavBar from "../src/components/NavBar";

export default {
  components: {
    NavBar,
  },
};
</script>

<style>
body {
  margin: 0;
  background-image: url("assets/vattendjungel.jpg");
  background-size: cover;
}

.container {
  width: 60%;
  min-height: 90vh;
  margin: 0 auto;
  background: lightgreen;
}

h1 {
  margin-top: 0;
  margin-bottom: 2rem;
  padding-top: 2rem;
  text-align: center;
}
</style>
