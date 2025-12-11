<script setup>



const projects = [
  { name: 'Tower', icons: '', imgPath: "", path_1: "https://tower.adamrb-portfolio.com", path_2: "https://github.com/AdamRB208/tower_2", description: "Tower is a fullstack application with a Vue front end and a Node.js back end. The application is designed to be a social media style of application where users can get posts from other users, create posts, delete and update their own content." },
  { name: 'Keepr', icons: '', imgPath: "", path_1: "https://keepr.adamrb-portfolio.com", path_2: "https://github.com/AdamRB208/keepr_dotnet_fullstack", description: "Keepr is a fullstack application with a Vue front end and a C# and SQL back end. The application is designed to be a social media style of application where users can get posts from other users, post, delete and update their own content." },
  // { name: 'Post-It', icons: '', imgPath: "", path_1: "", path_2: "https://github.com/AdamRB208/post_it_dotnet_fullstack", description: "Post It is a fullstack application with a Vue front end and a C# and SQL back end. The application is designed to be a social media style of application where users can get posts from other users, post, delete and update their own content." },
]

function liveAppClick(path_1) {
  window.open(path_1, '_blank');
}

function sourceCodeClick(path_2) {
  window.open(path_2, '_blank');
}


</script>


<template>
  <div v-for="project in projects" :key="project.name" class="col-md-6 text-center pe-0">
    <img
      src="https://plus.unsplash.com/premium_photo-1720032305135-a87c5e0888b6?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MzN8fHdlYiUyMGFwcGxpY2F0aW9uc3xlbnwwfHwwfHx8MA%3D%3D"
      :alt="project.name">
    <div class="fs-5 mt-2 mb-2">{{ project.name }}</div>
    <p>{{ project.description }}</p>
    <div class="d-flex justify-content-evenly mt-4">
      <button @click="liveAppClick(project.path_1)" class="btn btn-outline-success" type="button">Live
        Application</button>
      <button @click="sourceCodeClick(project.path_2)" class="btn btn-outline-success">Source Code</button>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.col-md-6 {
  padding-right: 0rem;
  padding-left: 1.5rem;
}
img {
  max-width: 400px;
  max-height: 400px;
  margin-top: 2rem;
}
</style>