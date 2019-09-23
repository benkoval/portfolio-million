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

<style lang='scss'>
$maingr: linear-gradient(to right, #D65394, #7C59AF, #3A5BAC, #FF6F61, #D65394);
$lato: 'Lato', sans-serif;
$lex: 'Playfair Display', serif;

.home {
  align-items: center;
  background-image: $maingr;
  background-size: 600%;
  background-position: 0 0;
  box-shadow: inset 0 0 5em rgba(0,0,0,.5);
  display: flex;
  flex-flow: column wrap;
  height: 100vh;
  justify-content: center;
  animation-duration: 20s;
  animation-iteration-count: infinite;
  animation-name: gradients;
}

.ghost {
  margin: auto;
  flex-direction: column;
  text-transform: uppercase;
  letter-spacing: 1.2px;
  font-size: 2rem;
  font-family: $lato;
  align-self: space-around;
  padding: 16px;
  color: #fff;
  border: 2px solid #fff;
  border-radius: 5px;
  text-align: center;
  outline: none;
  text-decoration: none;
  position: relative;
   -webkit-filter: drop-shadow(0 0 #105ccc);
  filter: drop-shadow(0 0 #105ccc);
  &:before {
    content: '';
    -webkit-transition: 0.4s all ease;
    transition: 0.4s all ease;
    position: absolute;
    top: 0;
    left: 50%;
    right: 50%;
    bottom: 0;
    opacity: 0;
    color: #105ccc;
    background-color: #fff;
    z-index:-2;
    border-radius: 5px;
  }
  &:hover, 
  &:focus-within {
    color: #105ccc;
    -webkit-transition: 0.4s all ease;
    transition: 0.4s all ease;
    &:before {
      -webkit-transition: 0.4s all ease;
      transition: 0.4s all ease;
      left: 0;
      right: 0;
      opacity: 1;
      border-radius: 3px;
    }
  }
}

.nav-button-container {
    display: flex;
    width: 75vw;
}
.title {
    font-family: $lex;
    text-align: center;
    font-size: 7rem;
    color: white;
    text-transform: uppercase;
}

@keyframes gradients {
    0%   {background-position: 0 0;}
    25% {background-position: 50% 0;}
    50% {background-position: 90% 0;}
    60% {background-position: 60%;}
    75% {background-position: 40%;}
    100%  {background-position: 0 0;}
}
</style>

<script>
import Nav from "./Nav";

export default {
  name: 'Home',
  components: {
    Nav
  }
}
</script>