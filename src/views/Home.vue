<template>
  <div class="home">
    <NavBar />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// @ is an alias to /srcf
// import HelloWorld from "@/components/HelloWorld.vue";
import NavBar from "@/components/NavBar.vue";

export default {
  name: "Home",
  components: {
    NavBar,
  },
};
</script>
