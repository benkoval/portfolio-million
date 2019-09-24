<template>
  <div id="app">
    <Nav/>
    <!-- <Home/> -->
    <About/>
    <Projects/>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'app',
  components: {
    Nav,
    Home,
    About,
    Projects
  }
}
</script>