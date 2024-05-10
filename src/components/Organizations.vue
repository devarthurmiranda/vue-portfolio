<template>
    <div class="card">
      <v-card-title>
        <h2>Organizations I contributed to</h2>
      </v-card-title>
      <v-card-text>
        <vueper-slides>
          <vueper-slide v-for="(org, index) in orgs" :key="index" :image="org.img">
          </vueper-slide>
        </vueper-slides>
      </v-card-text>
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
  .card {
    margin-left: 15%;
    margin-right: 15%;
    margin-top: 100px;
    padding: 20px;
    background-color: #323232;
    color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  </style>
  