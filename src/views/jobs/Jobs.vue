<template>
  <h1>I am jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{name: 'JobsDetails', params: {id: job.id}}">
        <p>{{ job.title }}</p>
    </router-link>
</div>
</template>

<script>
export default {
    data () {
        return {
            jobs: [
                {title: "Developer", id: "1", description: "logem"}, 
                {title: "Designer", id: "2", description: "logem"}, 
                {title: "Full Stack Engineer", id: "3", description: "logem"}, 
        ]
        }
      
    }

}
</script>

<style>

</style>