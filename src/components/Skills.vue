<template>
  <div class="container">
    <div class="row">
      <h2>Skills</h2>
      <div class="col-md-3" v-for="(skill, index) in skills" :key="index">
      <a href="">        
        <v-card>
          <v-card-title>
            <img :src="skill.icon" alt="" class="icon">
          </v-card-title>
          <v-card-text>
            <p>{{ skill.name }}</p>
          </v-card-text>
        </v-card>
      </a>

      </div>
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
  a {
    text-decoration: none;
    color: #ffffff;
  }

  .container {
    margin-top: 100px;
    margin-bottom: 50px;
  }

  h2 {
    text-align: center;
    color: #ffffff;
  }
  
  .row {
    max-width: 100%;
    text-align: center;
  }

  p {
    color: #ffffff;
  }
  
  .card {
    width: 100px;
    height: 100px;
    margin: 20px;
  }

  .icon{
    width: 50px;
    height: 50px;
  }
  </style>
  