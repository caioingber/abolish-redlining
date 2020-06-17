<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

a {
  font-weight: bold;
  color: black;
  text-decoration: none;
  border-bottom: 1px transparent black;
  &:hover {
    border-bottom: 1px solid black;
  }

  &.router-link-exact-active {
    // color: #42b983;
  }
}
</style>
