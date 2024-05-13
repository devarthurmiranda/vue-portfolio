<template>
    <div class="container">
        <h2>Worked with</h2>
        <vueper-slides fade :touchable="false">
            <vueper-slide v-for="(org, index) in orgs" :key="index" :image="org.img">
            </vueper-slide>
        </vueper-slides>
    </div>

</template>

<script>
import { VueperSlide, VueperSlides } from 'vueperslides';
import 'vueperslides/dist/vueperslides.css';
import orgs from '../../data/orgs.js';

export default {
    name: 'HomeOrganizations',
    components: {
        VueperSlides,
        VueperSlide
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
    margin-top: 100px;
    margin-bottom: 50px;
    width: 70%;
}

/* Text styles */
h2 {
    text-align: center;
    color: #ffffff;
}
</style>