<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import "@/global.scss";
* {
  box-sizing: border-box;
  margin: 0;
}
#app {
  font-family: "Open Sans", Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

a {
  font-weight: bold;
  color: black;
  text-decoration: none;
  border-bottom: 2px solid $nav-color;
  &:hover {
    border-bottom: 2px solid black;
    transition: 0.2s;
  }

  &.router-link-exact-active {
  }
}
</style>
