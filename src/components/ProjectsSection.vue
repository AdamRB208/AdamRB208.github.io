<script setup>
import ProjectCard from './ProjectCard.vue';


</script>


<template>
  <div class="col-12 d-flex justify-content-center mt-5" id="projects">
    <div class="d-block text-center" style="margin-bottom: 5rem;">
      <div class="fs-1" style="margin-bottom: 5rem;">Featured Projects</div>
      <p>Below are some of my more impressive fullstack applications and projects that I have built to date. The
        links to the source code and live projects are listed below.</p>
    </div>
  </div>
  <div class="row">
    <ProjectCard />
  </div>
</template>


<style lang="scss" scoped></style>