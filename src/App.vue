<template>
  <v-app>
    <v-main class="main">
      <HomePageVue />
    </v-main>
  </v-app>
</template>

<script setup>
import HomePageVue from "./components/HomePage.vue";
</script>

<style scoped>
.main {
  background-color: hsl(48, 71%, 99%);
}
</style>