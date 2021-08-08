<template>
  <div id="app">
    <nav>
      <p class="logo">My travel app</p>
      <ul class="nav-links">
        <li class="link">
          <router-link to="/">Home</router-link>
        </li>
        <li v-for="destination in destinations" :key="destination.name" class="link">
          <router-link :to="{name: 'DestinationDetails', params: {id:destination.id} }">{{destination.name}}</router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
  import store from "@/store"

  export default {
    data() {
      return {
        destinationId: this.$route.params.id,
        destinations: store.destinations
      }
    }
  }
</script>

<style scoped>
  nav {
    display: flex;
    justify-content: center;
  }

  nav a {
    color: #2c3e50;
    padding: 50px 10px;
    font-weight: bold;
    text-decoration: none;
  }

  nav a.router-link-exact-active {
    color: purple;
  }

  .nav-links {
    display: flex;
  }

  .link {
    padding-right: 20px;
    list-style: none;
  }

  .link:hover {
    text-decoration: underline;
  }
  .logo {
    font-size: 20px;
    color:purple;
    font-weight: bold;
  }



</style>