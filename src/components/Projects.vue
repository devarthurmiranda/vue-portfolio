<template>
  <div class="title">
    <h2>Projects</h2>
  </div>
  <div class="container-sm container">
    <Swiper>
      <SwiperSlide v-for="(project, index) in projects" :key="index">
        <v-card>
          <v-card-title><p>{{ project.name }}</p></v-card-title>
          <v-card-text>
            <p>{{ project.description }}</p>
            <img class="slide" :src="project.img" :alt="project.name">
          </v-card-text>
        </v-card>
      </SwiperSlide>
    </swiper>
  </div>

</template>

<script>
import projects from '../../data/projects.js';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

export default {
  name: 'HomeProjects',
  components: {
    Swiper,
    SwiperSlide,
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
  margin-top: 15%;
  width: 70%;
}


.slide{
  width: 70%;
  height: 10%;
  margin-left: 20px;
  margin-right: 20px;

}

.title{
  margin-bottom: 5%;
}

/* Text styles */
h2 {
  text-align: center;
  color: rgb(155, 74, 74);
  margin-bottom: 50px;
}

p {
  color: #ffffff;
}
</style>