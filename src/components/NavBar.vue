<template>
  <nav>
    <div class="nav-container">
      <a href="#">About Redlining</a>
      <a href="#">Reinvestment</a>
      <a href="#">Organizations</a>
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
