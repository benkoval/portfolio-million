<template>
    <section class='decidor-container'>
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
    </section>
</template>

<style lang='scss'>

.decidor-container {
    display: flex;
    justify-content: center;
    width: 100vw;
    height: 100vh;
}
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