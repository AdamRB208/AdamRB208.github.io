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
    <div class="container gap-2">
      <div class="d-flex align-items-center">
        <div class="d-flex justify-content-center">
          <span class="m-2">
            <a href="" class="fs-5">Home</a>
          </span>
          <span class="m-2">
            <a href="" class="fs-5">About Me</a>
          </span>
          <span class="m-2">
            <a href="" class="fs-5">Projects</a>
          </span>
          <span class="m-2">
            <a href="" class="fs-5">Contact</a>
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
    </div>
  </nav>
</template>

<style lang="scss" scoped>
a {
  text-decoration: none;
}


</style>
