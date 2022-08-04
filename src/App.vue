<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <br />
    <router-link to="/databinding/string">Databinding String</router-link> |
    <router-link to="/databinding/html">Databinding Html</router-link> |
    <router-link to="/databinding/input">Databinding Input</router-link> |
    <router-link to="/databinding/select">Databinding Select</router-link> |
    <router-link to="/databinding/checkbox">Databinding CheckBox</router-link> |
    <router-link to="/databinding/radio">Databinding RadioButton</router-link> |
    <router-link to="/databinding/attribute">Databinding Attribute</router-link>
    | <router-link to="/databinding/list">Databinding List</router-link> |
    <router-link to="/databinding/class">Databinding Class</router-link> |
    <router-link to="/databinding/style">Databinding Style</router-link> |
    <br />
    <router-link to="/event/click">Event Click</router-link> |
    <router-link to="/event/change">Event Change</router-link> |
    <router-link to="/event/key">Event Key</router-link> |
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
