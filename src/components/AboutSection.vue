<script setup>
import Portfolio_Image from '../assets/img/Portfolio_Image.png';
</script>


<template>
  <div class="col-12 d-block justify-content-center" id="about">
    <div class="d-flex justify-content-center mb-5 mt-5">
      <h1>About Adam Borup</h1>
    </div>
    <div class="row">
      <div class="col-md-5 d-flex justify-content-center">
        <div class="pt-5">
          <img :src="Portfolio_Image" alt="portfolio image of Adam Borup">
        </div>
      </div>
      <div class="col-md-7 d-flex justify-content-center">
        <div class="d-block">
          <div class="fw-bold text-center pb-2 mt-3">About Me</div>
          <p>My name is Adam Borup, I grew up in Boise Idaho and am happy to call it home. I am a proud husband and
            father to my wife Brianna and our two boys Mason and Malcolm. Growing up I spent a lot of time outside with
            my Grandfather hiking, fishing and camping so my love of the outdoors was engrained in me from a young age.
            I also loved playing on the computer and as a kid, we had all kinds of computer games and video game
            consoles so that was also a big part of my life. Throughout my life I have always loved working with
            computers. I enjoy learning how to use new software or features and finding new ways to take advantage of
            all of the things that they have to offer in everyday life.</p>
          <div class="fw-bold text-center pb-2">My Journey</div>
          <p>My journey into tech began when I took a free online course through Code School on HTML and CSS and
            JavaScript. I learned a lot from them but the most important thing I learned was how much I actually enjoyed
            software and web development and that I could see myself doing it as a career. I worked for a bank for
            almost 10 years and in late summer of 2024 they announced that they would be closing our site. While that
            was initially challenging I quickly realized that it was an opportunity to finally get into a software
            development job. Shortly after, a close friend recommend a local coding academy that offered a fullstack web
            development course and soon after I was signed up for the spring 2025 class at Boise CodeWorks Academy. On
            August 22, 2025 I got my certificate of achievement of their fullstack web developer course as a certified
            fullstack web developer.</p>
          <div class="fw-bold text-center pb-2">What I'm Working On</div>
          <p>Currently Im working on this portfolio website, getting the site and all of my applications that I have
            built live and included here in the website. After I have the website completed I plan to take a free course
            that Boise CodeWorks Academy offered to me after completing the fullstack course for Python. I enjoy
            learning new things when it comes to software development and I plan to constantly continue my learning
            journey with all that Python has to offer as well as thought my career as a software developer. Once I get a
            Python project started I plan to include it here and will make updates to the site as needed.</p>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
img {
  width: 300px;
  height: 400px;
  border-radius: 5%;
  object-fit: fill;
}
p {
  margin: 1.5em;
}
</style>