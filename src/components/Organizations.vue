<template>
    <div id="organizations" class="container-sm container">
        <div class="title">
            <h2>Empresas</h2>
        </div>
        <Swiper :pagination="{ dynamicBullets: true }" :modules="modules">
            <SwiperSlide v-for="(org, index) in orgs" :key="index">
                <div class="slideCard">
                    <a :href=org.link >
                        <h3>{{ org.name }}</h3>
                    </a>
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

.slideCard {
    width: 100%;
    padding: 32px 28px;
    border-radius: 24px;
    background: linear-gradient(135deg, rgba(36, 36, 36, 0.95), rgba(18, 18, 18, 0.95));
    border: 1px solid rgba(155, 74, 74, 0.35);
    box-shadow: 0 24px 45px rgba(0, 0, 0, 0.4);
    backdrop-filter: blur(8px);
    transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 18px;
    position: relative;
    overflow: hidden;
    margin: 10px;
    min-height: 320px;
}

.slideCard a {
    width: 100%;
}

.description {
    flex: 1;
    display: flex;
    align-items: center;
}

.slideCard::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 24px;
    background: radial-gradient(circle at top, rgba(155, 74, 74, 0.12), transparent 60%);
    opacity: 0;
    transition: opacity 0.3s ease;
    pointer-events: none;
    z-index: 0;
}

.slideCard:hover {
    transform: translateY(-6px);
    border-color: rgba(155, 74, 74, 0.65);
    box-shadow: 0 28px 55px rgba(155, 74, 74, 0.18);
}

.slideCard:hover::before {
    opacity: 1;
}

.slideCard > * {
    position: relative;
    z-index: 1;
}

.container {
    margin: 0 auto;
    text-align: center;
}

/* Small devices (landscape phones, 576px and up) */
@media screen and (max-width: 768px){
    .container {
        padding-top: 15%;
        width: 90%;
        text-align: center;
    }

    .slideCard {
        padding: 22px 20px;
        border-radius: 18px;
        min-height: 300px;
        gap: 14px;
    }

    .slideCard p {
        min-height: 64px;
    }
}

/* Medium devices (tablets, 768px and up) */
@media screen and (min-width: 768px){
    .container {
        padding-top: 15%;
        width: 70%;
        margin: 0 auto;
        text-align: center;
    }
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
    font-weight: 600;
    color: #f4f4f4;
    text-align: center;
    margin: 0;
    min-height: 46px;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

a {
    text-decoration: none;
    text-align: center;
    color: #f4f4f4;
    letter-spacing: 0.4px;
}

a:hover {
    text-decoration: none;
    color: rgb(155, 74, 74);
    transition: 300ms;
}

.slideCard p {
    color: #d7d7d7;
    margin: 0;
    line-height: 1.6;
    text-align: center;
    min-height: 72px;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

</style>
