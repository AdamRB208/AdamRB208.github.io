<script setup>
import AboutSection from '@/components/AboutSection.vue';
import ContactSection from '@/components/ContactSection.vue';
import HomeSection from '@/components/HomeSection.vue';
import ProjectsSection from '@/components/ProjectsSection.vue';
import SkillsSection from '@/components/SkillsSection.vue';




</script>

<!-- TODO go through all pages and make margins between sections consistent -->
<template>
  <section class="container-fluid">
    <!-- NOTE Home Section Starts Here -->
    <div class="row home-section home-bg" id="home">
      <HomeSection />
    </div>
    <!-- NOTE About Section Starts Here -->
    <div class="row about-section mt-5" id="about" style="height: auto;">
      <AboutSection />
    </div>
    <!-- NOTE Skills Section Starts Here -->
    <div class="row skills-section mt-5 mb-2" id="skills" style="height: auto;">
      <SkillsSection />
    </div>
    <!-- NOTE Projects Section Starts Here -->
    <div class="row projects-section mt-5 mb-2" id="projects" style="height: auto;">
      <ProjectsSection />
    </div>
    <!-- NOTE Contact Section Starts Here -->
    <div class="row contact-section" id="contact" style="margin-top: 1rem;">
      <ContactSection />
    </div>
  </section>
</template>

<style scoped lang="scss">
.container-fluid {
  max-width: 100%;
  overflow-x: hidden;
}
.home-bg {
  background-image: url(https://media.istockphoto.com/id/2165466401/photo/abstract-digital-wave-background.jpg?s=612x612&w=0&k=20&c=DquetIJzq1KoZWhr6RFlWrUmyBIYi6ilVGTUQBhL7hE=);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
      width: 100%;
        height: 100dvh;
        overflow-x: hidden;
}
</style>
