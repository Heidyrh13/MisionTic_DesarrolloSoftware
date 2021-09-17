<template>
  <v-container>
  <!--div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>-->
    <v-main>
    <router-view/>
    </v-main>
  <!--/div>-->
  </v-container>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #4ae2e7;

    &.router-link-exact-active {
      color: #1a8555;
    }
  }
}
</style>
