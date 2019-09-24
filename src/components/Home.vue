<template>
<div class='home'>
    <Nav/>
    <h1 class='title'>Hello, world!</h1>

    <div class='nav-button-container'>
        <!-- <a href='#projects' class='ghost'>Look at all my cool stuff!</a> -->
        
        <a href='#about-me' class='ghost'>Let me introduce myself</a>
    </div>
</div>
</template>

<script>
import Nav from "./Nav";

export default {
  name: 'Home',
  components: {
    Nav
  }
}
</script>