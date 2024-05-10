<template>
  <Navbar />
  <Intro />
  <About />
  <Organizations />
  <Skills />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Intro from './components/Intro.vue'
import About from './components/About.vue'
import Organizations from './components/Organizations.vue';
import Skills from './components/Skills.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Intro,
    About,
    Organizations,
    Skills
  },
  mounted() {
    this.changePageTitle('Portfolio');
  },
  methods: {
    changePageTitle(newTitle) {
      document.title = newTitle;
    }
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #181f25;
  margin-top: 60px;
  background-color: rgb(25, 25, 25);
}

::-webkit-scrollbar {
  width: 5px;
}

::-webkit-scrollbar-track {
  background: #17181a;
  border-radius: 9px;
  border: 2px solid #17181a;
  background-clip: content-box;
}

::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 9px;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>
