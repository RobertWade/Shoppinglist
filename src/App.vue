<template>
  <v-app id="app">
    <v-bottom-nav :value="true" fixed color="transparent">
      <v-btn color="teal" flat value="recent">
        <span>Notes</span>
        <v-icon>note</v-icon>
      </v-btn>
    </v-bottom-nav>
    <router-view/>
  </v-app>
</template>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
