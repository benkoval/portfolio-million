<template>
    <section 
    id='projects'>
        <div class='empty'></div>
        <h1 
        v-if='!hideProjects'
        class='proj-intro'>Projects</h1>
        <div 
        data-aos="zoom-in"
        data-aos-duration="1000"
        v-if='!hideProjects'
        class='projects-container'>
            <div class='grid-item a'>
                <button 
                @click='seeDecidor()'
                class='see-more wht a' type='button'>View project</button>
                <img class='deck-img' 
                alt='Homepage of decidOR app which displays a grid of activity choices, including watching movies or eating out' src='https://bean-project-screenshots.s3.amazonaws.com/decidor.png'/>
            </div>
            <div
            data-aos="zoom-in"
            data-aos-duration="1000"
            class='grid-item b'>
                <button
                @click='seeIpreview()' 
                class='see-more wht b' type='button'>View project</button>
                <img class='deck-img' 
                alt='iPreview search results' src='https://bean-project-screenshots.s3.amazonaws.com/ipreview.png'/>
            </div>
            <div
            data-aos="zoom-in"
            data-aos-duration="1000"
            class='grid-item e'>
                <button
                @click='seeFreeshelf()' 
                class='see-more wht e' type='button'>View project</button>
                <img 
                alt='Homepage of Freeshelf app' class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/freeshelf.png'/>
            </div>
            <div
            data-aos="zoom-in"
            data-aos-duration="1000"
            data-aos-offset="-300"
            class='grid-item d'>
                <button
                @click='seeCalculator()'
                class='see-more wht d' type='button'>Interactive</button>
                <img 
                alt='Calculator app' 
                class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/better-calculator.png'/>
            </div>
            <div
            data-aos="zoom-in"
            data-aos-duration="1000" 
            data-aos-offset="-350"
            class='grid-item c'>
                <button
                @click='seeYoga()'
                class='see-more wht c' type='button'>View project</button>
                <img 
                alt='Zen out homepage displays three yoga poses' class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ransom-asanas.png'/>
            </div>
            <div
            data-aos="zoom-in"
            data-aos-duration="1000"
            data-aos-offset="-400"
            class='grid-item d'>
                <button
                @click='seePokemon()' 
                class='see-more wht d' type='button'>Interactive</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/whos-that-pokemon.png'/>
            </div>
        </div>

        <div class='back-container' v-if='!hideDecidor'>
            <Decidor
            data-aos='fade-right'
            data-aos-duration='8000'/>
            <button 
            @click='backToProjs()'
            class='see-more fill a' 
            type='button'
            data-aos='fade-right'
            data-aos-duration='8000'
            data-aos-offset="-300">Back to projects</button>
            <div class='space'></div>
      </div>

        <div class='back-container' v-if='!hideIpreview'>
            <Ipreview
            data-aos='fade-right'
            data-aos-duration='8000'/>
            <button 
            data-aos='fade-right'
            data-aos-duration='8000'
            data-aos-offset="-300"
            @click='backToProjs()'
            class='see-more fill b' 
            type='button'>Back to projects</button>
            <div class='space'></div>
      </div>
        <div class='back-container' v-if='!hideCalculator'>
            <Calculator
            data-aos='fade-right'
            data-aos-duration='8000'/>
            <button 
            @click='backToProjs()'
            class='see-more fill d' 
            type='button'
            data-aos='fade-right'
            data-aos-duration='8000'
            data-aos-offset="-300">Back to projects</button>
            <div class='space'></div>
      </div>

      <div class='back-container' v-if='!hidePokemon'>
            <Pokemon
            data-aos='fade-right'
            data-aos-duration='8000'/>
            <button 
            @click='backToProjs()'
            class='see-more fill d' 
            type='button'
            data-aos='fade-right'
            data-aos-duration='8000'
            data-aos-offset="-300">Back to projects</button>
            <div class='space'></div>
      </div>

      <div class='back-container' v-if='!hideYoga'>
            <Yoga
            data-aos='fade-right'
            data-aos-duration='8000'/>
            <button 
            @click='backToProjs()'
            class='see-more fill c' 
            type='button'
            data-aos='fade-right'
            data-aos-duration='8000'
            data-aos-offset="-300">Back to projects</button>
            <div class='space'></div>
      </div>

        <div class='back-container' v-if='!hideFreeshelf'>
            <Freeshelf
            data-aos='fade-right'
            data-aos-duration='8000'/>
            <button 
            @click='backToProjs()'
            class='see-more fill e' 
            type='button'
            data-aos='fade-right'
            data-aos-duration='8000'
            data-aos-offset="-300">Back to projects</button>
            <div class='space'></div>
      </div>
    </section>
</template>

<script>
import { EventBus } from './event-bus.js';
import Decidor from "./Decidor";
import Ipreview from "./Ipreview";
import Calculator from "./Calculator";
import Pokemon from "./Pokemon";
import Yoga from "./Yoga";
import Freeshelf from "./Freeshelf";

export default {
  name: 'Projects',
  components: {
    Decidor,
    Ipreview,
    Calculator,
    Pokemon,
    Yoga,
    Freeshelf
  },
  data: () => {
    return {
        hideProjects: false,
        hideDecidor: true,
        hideIpreview: true,
        hideCalculator: true,
        hidePokemon: true,
        hideYoga: true,
        hideFreeshelf: true,
    }
  },
  mounted() {
    EventBus.$on('i-got-clicked', clicked => {
        this.backToProjs();
    });
  },
  methods: {
      backToProjs() {
          this.hideProjects = false;
          this.hideDecidor = true;
          this.hideIpreview  = true;
          this.hideCalculator = true;
          this.hidePokemon = true;
          this.hideYoga = true;
          this.hideFreeshelf = true;
      },
      seeDecidor() {
          this.hideProjects = true;
          this.hideDecidor = false;
      },
      seeIpreview() {
          this.hideProjects = true;
          this.hideIpreview = false;
      },
      seeCalculator() {
          this.hideProjects = true;
          this.hideCalculator = false;
      },
      seePokemon() {
          this.hideProjects = true;
          this.hidePokemon = false;
      },
      seeYoga() {
          this.hideProjects = true;
          this.hideYoga = false;
      },
      seeFreeshelf() {
          this.hideProjects = true;
          this.hideFreeshelf = false;
      }
  }
}
</script>