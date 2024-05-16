<template>
    <div id="organizations" class="container-sm container">
        <div class="title">
            <h2>Worked with</h2>
        </div>
        <Swiper :pagination="{dynamicBullets: true}" :modules="modules">
            <SwiperSlide v-for="(org, index) in orgs" :key="index">
                    <div class="slideCard">
                        <img class="img-fluid" :src="org.img" :alt="org.name"> 
                        <h3>{{ org.name }}</h3>
                    </div>   
            </SwiperSlide>
        </Swiper>
    </div>

</template>

<script>
import orgs from '../../data/orgs.js';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';

export default {
    name: 'HomeOrganizations',
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
            orgs: orgs
        };
    }
};
</script>

<style scoped>
.container {
    margin-top: 15%;
    width: 70%;
}

.swiper{
  text-align: center;
  padding: 20px;
}

.swiper-slide{
  display: flex;
  justify-content: center;
}

.slideCard{
  height: 400px;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
  background-color: #171717;
  padding: 20px;
  border-radius: 20px;
  margin: 10px;
}

.swiper-slide img{
  border-radius: 20px;
  max-width: 80%;
  max-height: 80%;
}

.title {
    margin-bottom: 5%;
}

.slides {
    max-width: 100%;
}

/* Text styles */
h2 {
    text-align: center;
    color: rgb(155, 74, 74);
}

h3 {
    text-align: center;
    color: #ffffff;
    margin-top: 5%;
}
</style>