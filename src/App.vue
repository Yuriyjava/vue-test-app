<template>
<v-app>
  <!-- Must have the app property -->
  <v-app-bar app>
    <v-btn :to="'/newUser'"  color="primary">Create User</v-btn>
  </v-app-bar>
  <v-main>
   <router-view/>
  </v-main>
</v-app>
 
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component({

})
export default class App extends Vue {
}
</script>
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
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
