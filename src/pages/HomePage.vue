<script setup>
import AboutSection from '@/components/AboutSection.vue';
import ContactSection from '@/components/ContactSection.vue';
import HomeSection from '@/components/HomeSection.vue';
import SkillsSection from '@/components/SkillsSection.vue';




</script>

<template>
  <section class="container-fluid">
    <!-- NOTE Home Section Starts Here -->
    <div class="row home-section home-bg" id="home" style="height: 100dvh;">
      <HomeSection />
    </div>
    <!-- NOTE About Section Starts Here -->
    <div class="row about-section" id="about" style="height: 100dvh;">
      <AboutSection />
    </div>
    <!-- NOTE Skills Section Starts Here -->
    <div class="row skills-section" id="skills">
      <SkillsSection />
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

<style scoped lang="scss">
.home-bg {
  background-image: url(https://media.istockphoto.com/id/2165466401/photo/abstract-digital-wave-background.jpg?s=612x612&w=0&k=20&c=DquetIJzq1KoZWhr6RFlWrUmyBIYi6ilVGTUQBhL7hE=);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
      width: 100dvw;
      height: 100dvh;
}
</style>
