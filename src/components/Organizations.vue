<template>
    <div class="container">
    <div class="card">
        <v-card-title>
            <h2>Worked with</h2>
        </v-card-title>
        <v-card-text>
            <vueper-slides fade :touchable="false">
                <vueper-slide v-for="(org, index) in orgs" :key="index" :image="org.img">
                </vueper-slide>
            </vueper-slides>
        </v-card-text>
    </div>
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
h2 {
    text-align: center;
    color: #ffffff;
}



.container {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px solid red;
}
.card {
    margin-top: 100px;
    background-color: #323232;
    color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 70%
}
</style>

<style>
.vueperslides__arrow {
    color: rgb(0, 0, 0)
}
</style>