<template>
  <div class="container-sm container">
    <div class="row">
      <div class="title">
        <h2>Tech Skills</h2>
      </div>
      
      <div id="skills" class="col-md-3" v-for="(skill, index) in skills" :key="index">
        <a :href="skill.wiki">
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
  margin-top: 15%;
  width: 70%;
  text-align: center;
}



.title {
  margin-bottom: 5%;
}

.card {
  width: 100px;
  height: 100px;
  margin-left: 20px;
  margin-right: 20px;
  margin-bottom: 20px;
}

/* Image styles */
.icon {
  width: 50px;
  height: 50px;
}

/* Text styles */
h2 {
  text-align: center;
  color: rgb(155, 74, 74);
  font-weight: bold;
}

.col-md-3 a {
    color: white;
    text-decoration: none;
}

.col-md-3 a:hover {
    text-decoration: none;
    color: rgb(155, 74, 74);
    transition: 400ms;
}
</style>