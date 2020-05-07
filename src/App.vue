<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Muli', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
  background: #eef6f9;
  width: 100vw;
}

::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar-track {
  background: whitesmoke;
  border-radius: 5px;
}

::-webkit-scrollbar-thumb {
  background: #0084b9a2;
  border-radius: 5px;
  display: none;
}

::-webkit-scrollbar-thumb:hover {
  display: block;
}

</style>
