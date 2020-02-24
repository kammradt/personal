<template>
  <v-app>
    <v-content class="clean">
      <v-container align-content-start>
        <router-view />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Lato");
#app {
  background-color: #ecf1fc;
  font-family: "Lato";
}
</style>