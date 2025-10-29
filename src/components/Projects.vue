<template>
  <div id="projects" class="container container-sm  w-70 p-3">
    <div class="title">
      <h2>Projetos</h2>
    </div>
    <Swiper :pagination="{dynamicBullets: true}" :modules="modules">
      <SwiperSlide v-for="(project, index) in projects" :key="index">
              <div class="slideCard">
                <a :href="project.link">
                    <img class="img-fluid" :src="project.img" :alt="project.name">
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

.container {
  margin: 0 auto;
  text-align: center;
}

.swiper{
  text-align: center;
  padding: 20px;
}

.slideCard{
  width: 100%;
  padding: 32px 28px;
  border-radius: 26px;
  background: linear-gradient(140deg, rgba(38, 38, 38, 0.96), rgba(18, 18, 18, 0.96));
  border: 1px solid rgba(155, 74, 74, 0.35);
  box-shadow: 0 24px 48px rgba(0, 0, 0, 0.42);
  backdrop-filter: blur(8px);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 18px;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
  position: relative;
  overflow: hidden;
  min-height: 420px;
  margin: 10px;
}

.slideCard::before{
  content: '';
  position: absolute;
  inset: 0;
  border-radius: 26px;
  background: radial-gradient(circle at top, rgba(155, 74, 74, 0.12), transparent 65%);
  opacity: 0;
  transition: opacity 0.3s ease;
  pointer-events: none;
  z-index: 0;
}

.slideCard:hover{
  transform: translateY(-6px);
  border-color: rgba(155, 74, 74, 0.65);
  box-shadow: 0 30px 56px rgba(155, 74, 74, 0.18);
}

.slideCard:hover::before{
  opacity: 1;
}

.slideCard > *{
  position: relative;
  z-index: 1;
}

.slideCard a{
  text-decoration: none;
  color: #f4f4f4;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 14px;
  width: 100%;
}

.slideCard h3{
  font-weight: 600;
  margin: 0;
  color: #f4f4f4;
  letter-spacing: 0.4px;
}

.slideCard img{
  width: 100%;
  max-width: 380px;
  height: 200px;
  border-radius: 18px;
  object-fit: cover;
  box-shadow: 0 18px 36px rgba(0, 0, 0, 0.45);
}

.slideCard p{
  color: #d7d7d7;
  margin: 0;
  line-height: 1.6;
  text-align: center;
  min-height: 96px;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.swiper-slide{
  display: flex;
  justify-content: center;
}



/* Text styles */
h2 {
  text-align: center;
  color: rgb(155, 74, 74);
  font-weight:600;
}

a {
  text-decoration: none;
  color: inherit;
  font-weight: 600;
}

a:hover {
  text-decoration: none;
  color: rgb(155, 74, 74);
  transition: 300ms;
}

p {
  color: #d7d7d7;
}

@media screen and (max-width: 768px){
  .container {
    width: 90%;
  }

  .slideCard{
    padding: 26px 22px;
    border-radius: 22px;
    min-height: 380px;
    margin: 10px 0;
  }
}

@media screen and (min-width: 768px){
  .container {
    width: 70%;
  }
}
</style>
