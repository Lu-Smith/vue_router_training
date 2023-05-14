<template>
  <h1>Jobs Details page</h1>
  <p>The jobs id is {{ id }}</p>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id
    }
  }
}
</script>

<style>

</style>