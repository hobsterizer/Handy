<template>
  <div id="Jobs">
    <div v-for="job in jobs" :key="job.id">
      <RouterLink :to="{ name: 'jobDetails', params:{id:job.id}}">
        {{ job.title }}
      </RouterLink>
    </div>
  </div>
</template>
<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Jobs",
  data() {
    return {
      jobs: [
        { title: "developer", id: 1, details: "ahmed" },
        { title: "marketing", id: 2, details: "ahmed" },
        { title: "Manegment", id: 3, details: "ahmed" },
      ],
    };
  },
};
</script>
<style scoped>
#Jobs{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#Jobs a{
  display: block;
  width:100px;
  margin: auto;
  margin-top: 10px;
  text-decoration: none;
  padding: 10px;
  background-color: lightblue;
  border-radius: 5px;
}
#Jobs a.router-link-exact-active{
  color: white;
  background-color: crimson;
}
</style>
