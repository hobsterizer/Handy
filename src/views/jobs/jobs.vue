<template>
  <div>
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
<style>

</style>
