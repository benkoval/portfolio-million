<template>
  <div id="app">
    <Nav/>
    <About/>
    <Resume/>
    <Projects/>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import Resume from './components/Resume.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'app',
  components: {
    Nav,
    Resume,
    About,
    Projects
  }
}
</script>