<script setup>
import { VueJS } from '../assets/icons/VueJS.svg';

const frontendIcons = [
  { name: 'VueJS', icon: 'VueJS.svg' }
];
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
        <button class="btn btn-glow" type="button" data-bs-toggle="collapse" data-bs-target="#collapseWidthExample"
          aria-expanded="false" aria-controls="collapseWidthExample">
          BackEnd Languages
        </button>
      </p>
      <p>
        <button class="btn btn-glow" type="button" data-bs-toggle="collapse" data-bs-target="#collapseWidthExample"
          aria-expanded="false" aria-controls="collapseWidthExample">
          Other Languages
        </button>
      </p>
    </div>
  </div>
  <div class="row">
    <div class="col d-flex justify-content-center">
      <div style="display: block;">
        <div class="collapse multi-collapse" id="frontendLanguages">
          <div class="card card-body" style="height: 300px;">
            This is some placeholder content for a horizontal collapse. It’s hidden by default and shown when
            triggered.
            <div v-for="skill in frontendIcons" :key="skill.name">
              <img :src="skill.icon" alt="skill.name">
              <div>{{ VueJS }}</div>
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
</style>