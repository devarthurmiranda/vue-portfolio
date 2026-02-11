<template>
    <div id="organizations" class="container-sm container">
        <div class="title">
            <h2>Companies</h2>
        </div>
        <Swiper :pagination="{ dynamicBullets: true }" :modules="modules" :breakpoints="breakpoints" class="swiper-container">
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
            breakpoints: {
                // Mobile
                320: {
                    slidesPerView: 1.2,
                    spaceBetween: 15
                },
                // Tablet
                640: {
                    slidesPerView: 2.2,
                    spaceBetween: 20
                },
                // Desktop
                1024: {
                    slidesPerView: 3.5,
                    spaceBetween: 25
                }
            }
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
.swiper-container {
    padding-bottom: 40px; /* Space for pagination */
}

.title h2 {
    margin-bottom: 30px; /* Reduced margin */
}

.swiper-slide {
    display: flex;
    justify-content: center;
    height: auto; /* Allow slide to determine height */
}

.slideCard {
    width: 100%;
    padding: 20px 16px; /* Reduced padding */
    border-radius: 16px; /* Smaller radius */
    background: linear-gradient(135deg, rgba(36, 36, 36, 0.95), rgba(18, 18, 18, 0.95));
    border: 1px solid rgba(155, 74, 74, 0.35);
    backdrop-filter: blur(8px);
    transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px; /* Reduced gap */
    justify-content: space-between;
    position: relative;
    overflow: hidden;
    height: 220px; /* Significantly reduced height from 360px */
}

.slideCard a {
    width: 100%;
    flex-shrink: 0;
}

.description {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
}

.slideCard::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 16px;
    background: radial-gradient(circle at top, rgba(155, 74, 74, 0.12), transparent 60%);
    opacity: 0;
    transition: opacity 0.3s ease;
    pointer-events: none;
    z-index: 0;
}

.slideCard:hover {
    transform: translateY(-4px); /* Subtle lift */
    border-color: rgba(155, 74, 74, 0.65);
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
    padding-top: 50px; /* Reduced top padding */
    padding-bottom: 50px;
}

/* Small devices (landscape phones, 576px and up) */
@media screen and (max-width: 768px){
    .container {
        padding-top: 10%;
        width: 95%; /* Wider on mobile */
        text-align: center;
    }

    .slideCard {
        padding: 16px 14px;
        border-radius: 14px;
        height: 200px; /* Even smaller on mobile */
        gap: 10px;
    }
}

/* Medium devices (tablets, 768px and up) */
@media screen and (min-width: 768px){
    .container {
        padding-top: 5%;
        width: 85%;
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
    font-size: 1.1rem; /* Slightly smaller font */
    min-height: auto; /* Remove fixed min-height */
    display: -webkit-box;
    -webkit-line-clamp: 1; /* Limit to 1 line if possible, or 2 */
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
    line-height: 1.4;
    text-align: center;
    font-size: 0.9rem; /* Smaller text */
    min-height: auto;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
    width: 100%;
}

</style>
