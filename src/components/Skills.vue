<template>
    <div class="row">
      <h2>Skills</h2>
      <div class="col-md-6" v-for="(skill, index) in skills" :key="index">
        <v-card>
          <v-card-title>
            <img :src="skill.icon" alt="" class="icon">
          </v-card-title>
          <v-card-text>
            <p>{{ skill.name }}</p>
          </v-card-text>
        </v-card>
      </div>
    </div>
  </template>
  
  <script>
  import skills from '../../data/skills.js';
  
  export default {
    name: 'HomeSkills',
    data() {
      return {
        skills: skills
      };
    }
  };
  </script>
  
  <style scoped>
  h2 {
    text-align: center;
    color: #ffffff;
  }
  
  .row {
    text-align: center;
    width: 100%;
    margin-top: 100px;
  }

  p {
    color: #ffffff;
  }
  
  .card {
    max-width: 100px;
    max-height: 100px;
    margin: 20px;
  }

  .icon{
    width: 50px;
    height: 50px;
  }
  </style>
  