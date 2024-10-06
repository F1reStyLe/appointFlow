<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <div class="left-links">
          <router-link to="/">Главная</router-link>
          <router-link to="/records">Записаться</router-link>
        </div>
        <div class="right-links">
          <button>Регистрация</button>
          <button>Вход</button>
        </div>
      </nav>
      <router-view/>
    </div>
  </header>
</template>

<style scoped>

</style>
