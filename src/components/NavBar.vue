<template>
  <nav>
    <div class="nav-container">
      <a href="#" target="_blank">About Redlining</a>
      <a href="#" target="_blank">Reinvestment</a>
      <a href="#" target="_blank">Organizations</a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style lang="scss" scoped>
@import "@/global.scss";

nav {
  background-color: $nav-color;
  height: 80px;
  @include flex(center, center, row);
  .nav-container {
    @include flex(space-between, center, row);
    width: 80%;
  }
}
</style>
