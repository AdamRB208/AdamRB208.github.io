<script setup>
import Portfolio_Image from '../assets/img/Portfolio_Image.png';
</script>


<template>
  <div class="col-12 d-block justify-content-center" id="about">
    <div class="d-flex justify-content-center mb-5 mt-5">
      <h1>About Adam Borup</h1>
    </div>
    <div>
    </div>
    <div class="row">
      <div class="col-md-5 d-flex justify-content-center">
        <div class="pt-5">
          <img :src="Portfolio_Image" alt="portfolio image of Adam Borup">
        </div>
      </div>
      <div class="col-md-7 d-flex justify-content-center ps-2 pe-5 mb-5">
        <div class="d-block">
          <div class="fw-bold text-center pb-2">About Me</div>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut omnis accusantium sapiente beatae voluptates,
            incidunt, quam debitis consectetur cumque optio quo tenetur amet tempora explicabo dolor ea minus culpa
            suscipit sit ad. Assumenda expedita, necessitatibus odit hic numquam, officiis facilis nam aliquam
            perspiciatis molestias blanditiis quaerat illum animi laboriosam pariatur voluptatibus dicta quos
            exercitationem eius consequatur doloremque rem eligendi maiores.</p>
          <div class="fw-bold text-center pb-2">My Journey</div>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Beatae, sed quibusdam natus aliquid labore
            voluptatem impedit suscipit cumque minima reprehenderit nesciunt consequuntur, aut ex iure quasi molestias
            repellat vero, esse nisi doloremque commodi inventore! Quod excepturi quia magnam cupiditate et, voluptatum
            quam, ipsa, eaque modi totam unde. Quia, ut nihil!</p>
          <div class="fw-bold text-center pb-2">What I'm Working On</div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia ipsa ut explicabo, doloribus iure eos
            neque? Impedit laudantium deserunt iste fugiat doloribus labore aut cumque! Laudantium vero delectus
            possimus neque, omnis voluptas voluptates natus. Laudantium velit recusandae ratione veritatis? Ipsam!</p>
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
</style>