<script setup>
import VueJS from '../assets/icons/VueJS.svg';
import JavaScript from '../assets/icons/JavaScript.svg';
import HTML from '../assets/icons/HTML.svg';
import CSS from '../assets/icons/CSS.svg';
import MongoDB from "../assets/icons/MongoDB.svg";
import MySQL from "../assets/icons/MySQL.svg";


const frontendIcons = [
  { name: 'VueJS', path: VueJS, description: "Vue is a progressive JavaScript framework used for building interactive user interfaces and single-page applications." },
  { name: 'JavasScript', path: JavaScript, description: 'JavaScript is a versatile programming language used to add interactivity and dynamic behavior to web pages.' },
  { name: 'HTML', path: HTML, description: "(HyperText Markup Language) is the standard language used to create and structure content on the web." },
  { name: 'CSS', path: CSS, description: "CSS (Cascading Style Sheets) is used to style and layout web pages, controlling colors, fonts, and spacing." }
];

const backendIcons = [
  { name: 'MongoDB', path: MongoDB, description: "MongoDB is a NoSQL database that stores data in flexible, JSON-like documents, making it easy to work with unstructured or semi-structured data." },
  { name: 'MySQL', path: MySQL, description: "MySQL is an open-source relational database management system that stores and organizes data in structured tables using SQL (Structured Query Language)." },

]
</script>


<template>
  <div class="col-12 d-flex justify-content-center mt-5" id="skills">
    <div class="d-block">
      <div class="fs-1 text-center">My Skills</div>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptas repellendus facilis illum
        quam esse
        consectetur vero eos tenetur error ut.</p>
    </div>
  </div>
  <div class="col-12 d-flex justify-content-center">
    <div class="d-flex justify-content-center">
      <p>
        <button class="btn btn-glow " type="button" data-bs-toggle="collapse" data-bs-target="#frontendLanguages"
          aria-expanded="false" aria-controls="frontendLanguages">
          FrontEnd Languages
        </button>
      </p>
      <p>
        <button class="btn btn-glow" type="button" data-bs-toggle="collapse" data-bs-target="#backendLanguages"
          aria-expanded="false" aria-controls="backendLanguages">
          BackEnd Languages
        </button>
      </p>
      <p>
        <button class="btn btn-glow" type="button" data-bs-toggle="collapse" data-bs-target="#collapseWidthExample"
          aria-expanded="false" aria-controls="collapseWidthExample">
          Other
        </button>
      </p>
    </div>
  </div>
  <div class="row">
    <div class="col d-flex justify-content-center">
      <div style="display: block;">
        <div class="collapse multi-collapse" id="frontendLanguages">
          <div class="card card-body flex-row justify-content-between mt-4"
            style="height: 300px; width: 100dvw; border: none;">
            <div v-for="icon in frontendIcons" :key="icon.name" class="frontEndIcons">
              <img :src="icon.path" :alt="icon.name">
              <p class="iconDesc">{{ icon.description }}</p>
            </div>
          </div>
        </div>
        <div class="collapse multi-collapse" id="backendLanguages">
          <div class="card card-body flex-row justify-content-between mt-4"
            style="height: 300px; width: 100dvw; border: none;">
            <div v-for="icon in backendIcons" :key="icon.name" class="frontEndIcons">
              <img :src="icon.path" :alt="icon.name">
              <p class="iconDesc">{{ icon.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>


<style lang="scss" scoped>
p {
  margin: 1.5em;
}
// p.iconDesc {
//   margin-left: 1em;
// }

img {
  width: 64px;
  height: 64px;
  ;
}

.frontEndIcons {
  display: grid;
  justify-items: center;
}

.iconDesc {
  max-width: 12em;
}
</style>