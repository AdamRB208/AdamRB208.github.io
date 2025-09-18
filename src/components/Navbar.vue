<script setup>
import { ref, watch } from 'vue';
import { loadState, saveState } from '../utils/Store.js';

const theme = ref(loadState('theme') || 'light')

function toggleTheme() {
  theme.value = theme.value == 'light' ? 'dark' : 'light'
}

watch(theme, () => {
  document.documentElement.setAttribute('data-bs-theme', theme.value)
  saveState('theme', theme.value)
}, { immediate: true })

</script>

<template>
  <nav class="navbar navbar-expand-md bg-codeworks border-bottom border-vue">
    <div class="container" style="display: flex; justify-content: space-evenly;">
      <div>
        <span class="m-2 nav-links">
          <a href="#home" class="mdi mdi-home-outline fs-5">Home</a>
          <a href="#about" class="mdi mdi-human-greeting-variant fs-5">About Me</a>
          <a href="#projects" class="mdi mdi-xml fs-5">Projects</a>
          <a href="#contact" class="mdi mdi-human-greeting-proximity fs-5">Contact</a>
        </span>
      </div>
    </div>

    <!-- THEME COMPONENT HERE -->
    <div class="ms-auto">
      <button class="btn text-light" @click="toggleTheme"
        :title="`Enable ${theme == 'light' ? 'dark' : 'light'} theme.`">
        <i v-if="theme == 'dark'" class="mdi mdi-weather-sunny"></i>
        <i v-if="theme == 'light'" class="mdi mdi-weather-night"></i>
      </button>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
a {
  text-decoration: none;
}
.nav-links {
  width: 100dvh;
  gap: 5em;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
nav {
  position: sticky;
  top: 0;
  z-index: 1020;
}
</style>
