<template>
    <section class='indiv-proj-container'>
      <h2 class='proj-title a'>decidOR</h2>
        <agile :autoplay='true'>
            <div class='slide'>
                <img class='proj-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor.png'>
            </div>

            <div class='slide'>
                <img class='proj-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor2.png'>
            </div>

            <div class='slide'>
                <img class='proj-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor3.png'>
            </div>

            <div class='slide'>
                <img class='proj-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor4.png'>
            </div>
        </agile>
        <div class='link-container'>
          <a class='links' target='blank' rel='noopener' href='https://github.com/decider-team/decidr'>Source code</a>
          <a class='links' target='blank' rel='noopener' href='https://decidor.herokuapp.com/'>Live site</a>
        </div>

        <div class='more-info'>
          <h3 class='proj-info'>Over the course of two weeks, I collaborated with three of my fellow developers at Momentum Learning to build decidOR, a web application which helps users handle the overwhelming experience of having too many decisions to make.
          We utilised various technologies, including <span class='tech a'>Django/Python, </span> <span class='tech b'>Vue/JavaScript, </span> <span class='tech c'>SCSS, </span> <span class='tech d'>Axios, </span> <span class='tech e'>AWS S3, </span> and more.</h3>
        </div>
    </section>
</template>

<style lang='scss'>
.agile {
    margin: auto;
    max-width: 40vw;
}
.agile__nav-button {
  background: transparent;
  border: none;
  color: #fff;
  cursor: pointer;
  font-size: 2rem;
  height: 100%;
  position: absolute;
  top: 0;
  transition-duration: 0.3s;
  width: 80px;
  filter: drop-shadow(2px 1px 1px #222);
}
.agile__nav-button:hover {
//   background-color: rgba(0, 0, 0, 0.5);
//   opacity: 1;
  transform: translateY(-.25em);
}
.agile__nav-button--prev {
  left: 0;
}
.agile__nav-button--next {
  right: 0;
}
.agile__dots {
//   bottom: 10px;
  left: 50%;
  position: absolute;
  transform: translateX(-50%);
//   filter: drop-shadow(2px 1px 1px #222);
}
.agile__dot {
  margin: 0 10px;
  & button {
    background-color: transparent;
    border: 1px solid #0a6cff;
    border-radius: 50%;
    cursor: pointer;
    display: block;
    height: .8vw;
    font-size: 0;
    line-height: 0;
    margin: 0;
    padding: 0;
    transition-duration: 0.3s;
    width: .8vw;
    &:hover {
        background-color: #63A4FF;
    }
  }
}
.agile__dot--current button {
  background-color: #63A4FF;
}

.slide {
  display: block;
}

.proj-img {
    width: 40vw;
}

</style>
<script>

import { VueAgile } from 'vue-agile'
 
export default {
    components: {
        agile: VueAgile
    }
}

</script>