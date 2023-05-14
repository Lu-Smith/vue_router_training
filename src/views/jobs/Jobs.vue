<template>
  <h1>I am jobs</h1>
  <div v-for="job in jobs" :key="job.id">
  <p>{{ job.title }}</p></div>
</template>

<script>
export default {
    data () {
        return {
            jobs: [
                {title: "Name 1", id: "1", description: "logem"}, 
                {title: "Name 2", id: "2", description: "logem"}, 
                {title: "Name 3", id: "3", description: "logem"}, 
        ]
        }
      
    }

}
</script>

<style>

</style>