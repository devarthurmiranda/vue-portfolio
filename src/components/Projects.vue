<template>
  <div class="container">
    <v-card>
      <v-card-title>
        <h2>Projects</h2>
      </v-card-title>
      <v-card-text>
        <vueper-slides class="no-shadow" :visible-slides="3" :slide-ratio="1 / 4" :dragging-distance="70">
          <vueper-slide v-for="(project, index) in projects" :key="index" :title="project.title"
            :image="project.img"></vueper-slide>
        </vueper-slides>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
import { VueperSlide, VueperSlides } from 'vueperslides';
import projects from '../../data/projects.js';
import 'vueperslides/dist/vueperslides.css';

export default {
  name: 'HomeProjects',
  components: {
    VueperSlides,
    VueperSlide
  },
  data() {
    return {
      projects: projects
    };
  }
}
</script>

<style scoped>
.container {
  margin-top: 100px;
  width: 70%;
}

/* Text styles */
h2 {
  text-align: center;
  color: #ffffff;
  margin-bottom: 50px;
}

p {
  color: #ffffff;
}
</style>