<template>
  <div id="app">
    
    <Search />
    <Film />
  </div>
</template>

<script>
import Search from './components/Search.vue';
import Film from "./components/Film.vue";

export default {
  name: 'App',
  components: {
    Search,
    Film
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
