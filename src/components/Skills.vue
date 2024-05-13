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
.container {
  margin-top: 100px;
  margin-bottom: 50px;
}

.row {
  max-width: 100%;
  text-align: center;
}

.card {
  width: 100px;
  height: 100px;
  margin: 20px;
}

/* Image styles */
.icon {
  width: 50px;
  height: 50px;
}

/* Text styles */
h2 {
  text-align: center;
  color: #ffffff;
}

a {
  text-decoration: none;
  color: #ffffff;
}

p {
  color: #ffffff;
}
</style>