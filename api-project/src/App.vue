<template>
  <div id="app">
    <div id="nav">
      <router-link class="nav-text" to="/">Movie</router-link>
      <router-link class="nav-text" to="/search">Search</router-link>
      <router-link class="nav-text" to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kanit:ital,wght@0,200;0,400;1,100;1,400&display=swap');

* {
  margin: 0;
  padding: 0;
  font-family: 'Kanit', sans-serif;
}
#nav {
  width: 100%;
  background-color: grey;
  font-weight: 400;
}
.nav-text {
  margin: 0 0.5rem 0 0.5rem;
  text-decoration: none;
  color: black;

  font-size: 1.25rem;
}
.nav-text:hover {
  color: antiquewhite;
  transition: 0.1s;

}
</style>
