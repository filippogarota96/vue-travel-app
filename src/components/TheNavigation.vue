<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/brazil">Brazil</router-link>
      <router-link to="/hawaii">Hawaii</router-link>
      <router-link to="/jamaica">Jamaica</router-link>
      <router-link to="/panama">Panama</router-link>

    </nav>
  </div>
</template>

<style scoped>
  nav {
    display: flex;
    justify-content: center;
  }

  nav a {
    font-weight: bold;
    color: #2c3e50;
    padding: 50px 10px;
  }

  nav a.router-link-exact-active {
    color: red;
  }
</style>