<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="menu py-3 lg:px-44 gap-4 md:gap-14 flex flex-wrap items-center justify-center lg:justify-between bg-black text-slate-200">
      <div class="brand flex items-center gap-1">
        <img src="./assets/logo.svg" alt="universo" class="w-14">
        <span class="font-bold text-purple-600 text-xl">Universo</span>
      </div>
      <nav class="gap-8 flex text-lg">
        <RouterLink to="/" class="font-semibold hover:text-purple-600">Inicio</RouterLink>
        <RouterLink to="/planetas" class="font-semibold hover:text-purple-600">Planetas</RouterLink>
        <RouterLink to="/about" class="font-semibold hover:text-purple-600">About</RouterLink>
      </nav>
      <div class="redes gap-3 flex">
        <a href="https://web.facebook.com/profile.php?id=100082436926740"><img src="./assets/facebook.svg" alt="facebook" class="w-7"></a>
        <a href="https://github.com/Denzel-James"><img src="./assets/github.svg" alt="github" class="w-7"></a>
        <a href="#"><img src="./assets/youtube.svg" alt="youtube" class="w-7"></a>
      </div>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
</style>
