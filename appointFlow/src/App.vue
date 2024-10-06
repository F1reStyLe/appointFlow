<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/home">Home</RouterLink>
        <RouterLink to="/records">Records</RouterLink>
      </nav>
      <router-view/>
    </div>
  </header>
</template>

<style scoped>

</style>
