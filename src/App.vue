<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="container">
      <nav class="nav bg-dark">
        <RouterLink class="nav-link active" aria-current="page" to="/" >Inicio</RouterLink>
        <RouterLink class="nav-link" to="/producto">Producto</RouterLink>

      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
</style>
