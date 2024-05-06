<template>
  <Navbar />

  <Footer />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
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

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #181f25;
  margin-top: 60px;
}
</style>
