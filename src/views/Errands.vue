<template>
  <main id="errands">
    <MainNavBar></MainNavBar>
  </main>
</template>

<script>
import MainNavBar from "../components/MainNavbar";

export default {
  components: {
    MainNavBar
  }
};
</script>

<style scoped>
* {
  color: #666666;
}
body {
  height: 100vh;
  background-color: #eef6f9;
}

</style>