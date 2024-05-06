<template>
  <Navbar />
  <Intro />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Intro from './components/Intro.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Intro,
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
</style>
