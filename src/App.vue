<template>
  <div id="app">
    <Home/>
    <Projects/>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'app',
  components: {
    Home,
    Projects
  }
}
</script>