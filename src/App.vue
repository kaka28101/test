<template>
  <div class="container" id="app">
    <navbar></navbar>
    <router-view></router-view>
    <login></login>
  </div>
</template>

<script>
  import Navbar from './components/Navbar.vue'
  import Login from './components/authentication/Login.vue'
export default {
  components :{
    'navbar': Navbar,
    'login': Login
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
