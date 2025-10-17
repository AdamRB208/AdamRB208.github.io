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
  <nav class="container-fluid navbar navbar-expand-md bg-codeworks">
    <div>
      <div>
        <!-- TODO get the links to show in a dropdown when screen size goes below X size -->
        <span class="nav-links">
          <a href="#home" class="mdi mdi-home-outline font-glow fs-5 p-3"> Home</a>
          <a href="#about" class="mdi mdi-human-greeting-variant fs-5 p-3"> About Me</a>
          <a href="#skills" class="mdi mdi-karate fs-5 p-3">Skills</a>
          <a href="#projects" class="mdi mdi-xml fs-5 p-3"> Projects</a>
          <a href="#contact" class="mdi mdi-human-greeting-proximity fs-5 p-3"> Contact</a>
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
  color: #87beb8;
    ;
}
.nav-links {
  gap: 1em;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
}
nav {
  position: sticky;
  top: 0;
  z-index: 1020;
  height: auto;
  padding: 0;
}
i {
  color: #87beb8;
}
.container-fluid {
  max-width: 100%;
  overflow-x: hidden;
}
</style>
