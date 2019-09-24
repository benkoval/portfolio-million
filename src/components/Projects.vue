<template>
    <section id='projects'>
        <div 
        v-if='!hideProjects'
        class='projects-container'>
            <div class='grid-item a'>
                <button 
                @click='seeDecidor()'
                class='see-more wht a' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor.png'/>
            </div>
            <div class='grid-item b'>
                <button class='see-more wht b' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ipreview.png'/>
            </div>
            <div class='grid-item c'>
                <button class='see-more wht c' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ransom-asanas.png'/>
            </div>
            <div class='grid-item d'>
                <button class='see-more wht d' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/better-calculator.png'/>
            </div>
            <div class='grid-item e'>
                <button class='see-more wht e' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/freeshelf.png'/>
            </div>
            <div class='grid-item b'>
                <button class='see-more wht b' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/whos-that-pokemon.png'/>
            </div>
        </div>

        <div class='back-container' v-if='!hideDecidor'>
            <button 
            @click='backToProjs()'
            class='see-more clr a' type='button'>Back to projects</button>
            <Decidor/>
      </div>
    </section>
</template>

<script>
import Decidor from "./Decidor";

export default {
  name: 'Projects',
  components: {
    Decidor
  },
  data: () => {
    return {
        hideProjects: false,
        hideDecidor: true
    }
  },
  methods: {
      backToProjs() {
          this.hideProjects = false;
          this.hideDecidor = true;
      },
      seeDecidor() {
          this.hideProjects = true;
          this.hideDecidor = false;
      }
  }
}
</script>