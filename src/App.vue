<template>
  <Navbar />
  <Intro />
  <About />
  <Organizations />
  <Projects />
  <Skills />
  <Footer />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Intro from './components/Intro.vue'
import About from './components/About.vue'
import Organizations from './components/Organizations.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Intro,
    About,
    Organizations,
    Projects,
    Skills,
    Footer
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
/**App Style */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #181f25;
  background-color: rgb(25, 25, 25);
  padding-top: 60px;
}

/**Scrollbar style */
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
