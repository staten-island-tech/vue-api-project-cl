<template>
  <div id="app">
    <div id="nav">
      <router-link class="nav-text" to="/">Home</router-link>
      <router-link class="nav-text" to="/search">Search</router-link>
      <router-link class="nav-text" to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}
#nav {
  width: 100%;
  background-color: grey;
}
.nav-text {
  margin: 0 0.5rem 0 0.5rem;
  text-decoration: none;
  color: black;

  font-size: 2rem;
}
.nav-text:hover {
  color: antiquewhite;
  transition: 0.1s;
}
</style>
