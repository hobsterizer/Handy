<template>
  <div id="app">
    <RouterLink to="/">Home</RouterLink> |
    <RouterLink :to="{ name: 'About' }">About</RouterLink> | 
    <RouterLink :to="{ name: 'jobs' }">Jobs</RouterLink>
  </div>
  <RouterView/>
</template>

<script>
export default {
  name: 'App',

}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#app a{
  text-decoration: none;
  padding: 10px;
  background-color: lightblue;
  border-radius: 5px;
}
#app a.router-link-exact-active{
  color: white;
  background-color: crimson;
}
#app a.router-link-active{
  color: white;
  background-color: crimson;
}
</style>
