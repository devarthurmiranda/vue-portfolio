<template>
    <div id="organizations" class="container-sm container">
        <div class="title">
            <h2>Empresas</h2>
        </div>
        <Swiper :pagination="{ dynamicBullets: true }" :modules="modules">
            <SwiperSlide v-for="(org, index) in orgs" :key="index">
                <div class="slideCard">
                    <img class="img-fluid" :src="org.img" :alt="org.name">
                    <a href=""><h3>{{ org.name }}</h3></a>
                    <div class="description">
                        <p>{{ org.occupation }}</p>
                    </div>
                    
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
.swiper {
    text-align: center;
    padding: 20px;
}

.swiper-slide {
    display: flex;
    justify-content: center;
}

/* Small devices (landscape phones, 576px and up) */
@media screen and (max-width: 768px){
    img {
        height: 50px;
        width: 60%;
    }

    .container {
        padding-top: 15%;
        width: 90%;
    }

    .slideCard {
        height: 400px;
        width: 100%;
        box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
        background-color: #171717;
        padding: 20px;
        border-radius: 20px;
        margin: 10px;
    }
}

/* Medium devices (tablets, 768px and up) */
@media screen and (min-width: 768px){
    img {
        height: 50%;
        width: 60%;
    }

    .slideCard {
        height: 400px;
        width: 100%;
        box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
        background-color: #171717;
        padding: 20px;
        border-radius: 20px;
        margin: 10px;
    }
    .container {
        padding-top: 15%;
        width: 70%;
    }
}


.swiper-slide img {
    border-radius: 20px;
    max-width: 100%;
    max-height: 90%;
}

.slides {
    max-width: 100%;
}

/* Text styles */
h2 {
    text-align: center;
    color: rgb(155, 74, 74);
    font-weight: 600;
}

h3 {
    margin-top: 2%;
    font-weight: 600;
}

a {
    text-decoration: none;
    text-align: center;
    color: #ffffff;
    
}

a:hover {
    text-decoration: none;
    color: rgb(155, 74, 74);
    transition: 300ms;
}

.slideCard p {
    color: #ffffff;
    margin-left: 10%;
    margin-right: 10%;
}

</style>