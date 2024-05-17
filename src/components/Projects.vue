<template>
  <div id="projects" class="container container-sm  w-70 p-3">
    <div class="title">
      <h2>Projetos</h2>
    </div>
    <Swiper :pagination="{dynamicBullets: true}" :modules="modules">
      <SwiperSlide v-for="(project, index) in projects" :key="index">
              <div class="slideCard">
                  <img class="img-fluid" :src="project.img" :alt="project.name"> 
              <a :href="project.link">
                <h3>{{ project.title }}</h3>
              </a>
                <p>{{ project.description }}</p>
              </div>   
      </SwiperSlide>
    </Swiper>
  </div>

</template>

<script>
import projects from '../../data/projects.js';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';


export default {
  name: 'HomeProjects',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
  data() {
    return {
      projects: projects
    };
  }
}
</script>

<style scoped>
#projects {
  margin-top: 15%;
}

@media screen and (max-width: 768px){
  .slideCard{
    height: 350px;
    width: 100%;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
    background-color: #191919;
    padding: 20px;
    border-radius: 20px;
    margin: 10px;
  }

  .container {
    width: 90%;
  }
}

@media screen and (min-width: 768px){
  .slideCard{
    height: 400px;
    width: 100%;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
    background-color: #191919;
    padding: 20px;
    border-radius: 20px;
    margin: 10px;
  }

  .container {
    width: 70%;
  }


}



.swiper{
  text-align: center;
  padding: 20px;
}

.swiper-slide{
  display: flex;
  justify-content: center;
}



.swiper-slide img{
  border-radius: 20px;
  max-width: 80%;
  max-height: 80%;
}

.slide{
  width: 400px;
  height: 400px;
} 

/* Text styles */
h2 {
  text-align: center;
  color: rgb(155, 74, 74);
  font-weight:600;
}

h3 {
  font-weight: 600;
}

a {
  text-decoration: none;
  color: #ffffff;
  font-weight: 600;
}

a:hover {
  text-decoration: none;
  color: rgb(155, 74, 74);
  transition: 300ms;
}

p {
  color: #ffffff;
}
</style>