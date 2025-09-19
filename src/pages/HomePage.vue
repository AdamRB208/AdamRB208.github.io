<script setup>
import ContactSection from '@/components/ContactSection.vue';




</script>

<template>
  <section class="container">
    <!-- NOTE Home Section Starts Here -->
    <div class="row home-section" id="home" style="height: 100dvh;">
      <div class="col-12 d-flex justify-content-center mt-5" id="home">
        <div>home section</div>
      </div>
    </div>
    <!-- NOTE About Section Starts Here -->
    <div class="row about-section" id="about" style="height: 100dvh;">
      <div class="col-12 d-flex justify-content-center mt-5" id="about">
        <span>
          <h1>About Adam Borup</h1>
        </span>
      </div>
    </div>
    <!-- NOTE Projects Section Starts Here -->
    <div class="row projects-section" id="projects" style="height: 100dvh;">
      <div class="col-12 d-flex justify-content-center mt-5" id="projects">
        <span>
          <h2>Featured Projects</h2>
        </span>
      </div>
    </div>
    <!-- NOTE Contact Section Starts Here -->
    <div class="row contact-section" id="contact" style="height: 100dvh;">
      <ContactSection />
    </div>
  </section>
</template>

<style scoped lang="scss"></style>
