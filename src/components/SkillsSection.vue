<script setup>
import VueJS from '../assets/icons/VueJS.svg';
import JavaScript from '../assets/icons/JavaScript.svg';
import HTML from '../assets/icons/HTML.svg';
import CSS from '../assets/icons/CSS.svg';
import MongoDB from "../assets/icons/MongoDB.svg";
import MySQL from "../assets/icons/MySQL.svg";
import cSharp from "../assets/icons/c-sharp.png";
import NodeJS from "../assets/icons/NodeJs.svg";
import Auth0 from "../assets/icons/Auth0.svg";
import Docker from "../assets/icons/Docker.svg";
import Figma from "../assets/icons/Figma.svg";
import { Collapse } from 'bootstrap';
import { logger } from '@/utils/Logger.js';


const frontendIcons = [
  { name: 'VueJS', path: VueJS, description: "Vue is a progressive JavaScript framework used for building interactive user interfaces and single-page applications." },
  { name: 'JavasScript', path: JavaScript, description: 'JavaScript is a versatile programming language used to add interactivity and dynamic behavior to web pages.' },
  { name: 'HTML', path: HTML, description: "(HyperText Markup Language) is the standard language used to create and structure content on the web." },
  { name: 'CSS', path: CSS, description: "CSS (Cascading Style Sheets) is used to style and layout web pages, controlling colors, fonts, and spacing." }
];

const backendIcons = [
  { name: 'MongoDB', path: MongoDB, description: "MongoDB is a NoSQL database that stores data in flexible, JSON-like documents, making it easy to work with unstructured or semi-structured data." },
  { name: 'MySQL', path: MySQL, description: "MySQL is an open-source relational database management system that stores and organizes data in structured tables using SQL (Structured Query Language)." },
  { name: 'cSharp', path: cSharp, description: "C# is a modern, object-oriented programming language developed by Microsoft for building a wide range of applications on the .NET platform." },
  { name: 'NodeJs', path: NodeJS, description: "Node.js is a runtime environment that allows you to run JavaScript code on the server side, enabling backend development with JavaScript." }
];

const otherIcons = [
  { name: 'Auth0', path: Auth0, description: "Auth0 is an authentication and authorization platform that enables developers to easily add secure login and identity management to their applications." },
  { name: 'Docker', path: Docker, description: "Docker is a platform that allows developers to package applications and their dependencies into containers, making them easy to build, ship, and run across different environments." },
  { name: 'Figma', path: Figma, description: "Figma is a collaborative web-based design tool that allows teams to create, prototype, and share user interface designs in real time." }
]

function closeOtherSections(currentSectionId) {
  const allSelectionIds = ['frontendBtn', 'backendBtn', 'otherBtn'];
  allSelectionIds.forEach(id => {
    const elemName = document.getElementById(id);
    if (elemName) {
      const collapseInstance = Collapse.getOrCreateInstance(elemName);
      collapseInstance.hide();
      logger.log('elemName', elemName)
    }
  });
  const currentElemName = document.getElementById(currentSectionId);
  if (currentElemName) {
    const collapseInstance = Collapse.getOrCreateInstance(currentElemName);
    collapseInstance.show();
    logger.log('currentElemName', currentElemName)
  }
}

function buttonClick(event, currentSectionId) {
  event.preventDefault();
  event.stopPropagation();
  closeOtherSections(currentSectionId);
}

</script>


<template>
  <div class="col-12 d-block justify-content-center" id="skills">
    <div>
      <div class="fs-1 text-center" style="margin-bottom: 5rem;">My Skills</div>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Enim eligendi, excepturi perspiciatis delectus
        dignissimos laboriosam blanditiis alias nemo culpa officia sint esse eum porro in consectetur! Eveniet
        quisquam
        perspiciatis ullam ipsam ratione culpa necessitatibus amet. Dolorum iusto quae nihil libero dolores labore,
        voluptatibus praesentium consectetur ab sequi soluta dignissimos explicabo?</p>
    </div>
  </div>
  <div class="d-flex justify-content-center">
    <p>
      <button @click.prevent="buttonClick($event, 'frontendBtn')" class="btn btn-glow text-center" type="button"
        data-bs-target="#frontendBtn" aria-expanded="false" aria-controls="frontendBtn"><i
          class="mdi mdi-monitor-cellphone fs-4 text-center"></i>
        Frontend
      </button>
    </p>
    <p>
      <button @click.prevent="buttonClick($event, 'backendBtn')" class="btn btn-glow" type="button"
        data-bs-target="#backendBtn" aria-expanded="false" aria-controls="backendBtn"><i
          class="mdi mdi-database-outline fs-4 text-center"></i>
        Backend
      </button>
    </p>
    <p>
      <button @click.prevent="buttonClick($event, 'otherBtn')" class="btn btn-glow text-center" type="button"
        data-bs-target="#otherBtn" aria-expanded="false" aria-controls="otherBtn"><i
          class="mdi mdi-source-branch fs-4 text-center"></i>
        Other
      </button>
    </p>
  </div>
  <div class="collapse" id="frontendBtn">
    <div class="card card-body flex-row justify-content-evenly mt-4"
      style="height: 300px; width: 100dvw; border: none;">
      <div v-for="icon in frontendIcons" :key="icon.name" class="icons">
        <img :src="icon.path" :alt="icon.name">
        <p class="iconDesc">{{ icon.description }}</p>
      </div>
    </div>
  </div>
  <div class="collapse" id="backendBtn">
    <div class="card card-body flex-row justify-content-evenly mt-4"
      style="height: 300px; width: 100dvw; border: none;">
      <div v-for="icon in backendIcons" :key="icon.name" class="icons">
        <img :src="icon.path" :alt="icon.name">
        <p class="iconDesc">{{ icon.description }}</p>
      </div>
    </div>
  </div>
  <div class="collapse" id="otherBtn">
    <div class="card card-body flex-row justify-content-evenly mt-4"
      style="height: 300px; width: 100dvw; border: none;">
      <div v-for="icon in otherIcons" :key="icon.name" class="icons">
        <img :src="icon.path" :alt="icon.name">
        <p class="iconDesc">{{ icon.description }}</p>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
p {
  margin: 1.5em;
}


img {
  width: 64px;
  height: 64px;
  ;
}

.icons {
  display: grid;
  justify-items: center;
}

.iconDesc {
  max-width: 12em;
}
</style>
<!-- TODO dont forget to copy link in the credits section or similar section for attribute for icon. -->
<!-- <a href="https://www.flaticon.com/free-icons/c-sharp" title="c sharp icons">C sharp icons created by Freepik - Flaticon</a> -->