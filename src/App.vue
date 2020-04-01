<template>
  <div class="container">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>

    <hr />

    <HelloWorld />

    <router-view />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue"
/*
  You cannot access $router or $route with the new Vue Router, Instead we do use useRoute() and useRouter() functions from the vue-router like this :

  import { useRoute, useRouter } from "vue-router"

  then we can access it in the setup() method like this:

  setup() {
    const route = useRoute()
    const router = useRouter()
  }
*/

export default {
  components: { HelloWorld }
}
</script>

<style lang="scss">
.container {
  width: 80%;
  margin: 0 auto;
  text-align: center;
  color: #35495e;
  font-family: monospace;

  a {
    font-size: 1rem;
    text-decoration: none;
    display: inline-block;
    padding: 0.3rem 1rem;
    border-radius: 0.3rem;
    color: #35495e;
    transition: 0.25s ease-in-out;

    &.router-link-exact-active {
      background: #41b883;
      color: white;
    }
  }
}
</style>
