<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{name:'About'}">About</router-link>
    <router-link :to="{name:'Jobs'}">Jobs</router-link>
  </nav>
  <div class="buttons">
    <button @click="redirect" >Redirect</button>
    <button @click="back">Go back</button>
    <button @click="forward">Go forward</button>
  </div>
  <router-view/>
</template>

<script>
export default {
  methods: {
redirect() {

},
back() {
this.$router.go(-1)
},
forward() {
this.$router.go(1)
}
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 10px;
}

nav a.router-link-exact-active {
  color: #ecf3f0;
  background: crimson;
}

.buttons{
  height: 80px;
}

button {
  margin: 0 10px;
  padding: 10px;
  border: none;
  border-radius: 4px;
  box-sizing: border-box;
  transition: 200ms all ease-in-out;
}

button:hover {
  border-bottom: 2px solid black;
  background: rgb(185, 183, 183);
}

</style>
