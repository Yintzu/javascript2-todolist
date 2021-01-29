<template>
  <div class="navbar">
      <h1 class="name">Victor Werngren</h1>
    <router-link to="/" class="navlink">Home</router-link>
    <router-link to="/about" class="navlink">About</router-link>
    <router-link to="/addnew" class="navlink">Add New</router-link>
  </div>
</template>

<style>
.navbar {
  display: flex;
  justify-content: center;
  align-items: center;
  background: green;
  height: 10vh;
}

.navlink {
  font-weight: bold;
  margin: 0 10px;
  color: black;
  background: lightgreen;
  padding: 10px;
  font-family: sans-serif;
  text-decoration: none;
  box-shadow: 0px 0px 5px;
}

.navlink:hover {
  background: rgb(178, 236, 178);
}

.name{
    position: absolute;
    left: 25px;
    margin-right: 30vw;
}
</style>