<template>
    <section 
    id='resume'
    class='skills-container'>
    <div class='empty'></div>
      <ul class='proj-intro'>Skills</ul>
      <div class='container-of-container'>
          <div class='list-container'>
            <li 
            data-aos="zoom-in-right"
            class='li-skill'>Django</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill'>React</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill'>HTML</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill'>SCSS</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill'>JavaScript</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill'>Python</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill'>GitHub</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill'>Vue</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill'>Postgres</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill'>Heroku</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill'>AWS S3</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill'>Surge</li>
          </div>
        </div>
    <h3
    data-aos="fade-right"
    data-aos-offset='-300'
    class='placeholder-res'>Check out my <a id='resume-link' target='blank' rel='noopener' href='https://drive.google.com/file/d/1tXcFxAAXBADAPovT5fiUc58io0Q50Gls/view'>resume</a></h3>

            <!-- <div class='grid-1'>
                <button class='see-more wht' role='button'>View resume</button>
            </div> -->
        <!-- <object 
        data-aos="fade"
        data-aos-duration="1500" 
        class='resume' data='https://bean-project-screenshots.s3.amazonaws.com/bkoval-resume-21-9.pdf'></object> -->
    </section>
</template>

<style lang='scss'>

.skill-grid {
  display: grid;
  grid-template-rows: repeat(2, 1fr);
  grid-template-columns: repeat(4, 1fr);
  width: 100vw;
  height: 100vh;
  @media screen and (max-width: 60em) {
    grid-template-rows: repeat(4, 1fr);
  }
}

// .grid-1,
// .grid-2,
// .grid-3,
// .grid-4 {
//   grid-template-rows: repeat(6, 1fr);
//   grid-template-columns: repeat(6, 1fr);
// }
.grid-1 {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row: 1;
  @media screen and (max-width: 60em) {
    grid-column-start: 1;
    grid-column-end: 5;
    grid-row: 1;
  }
}

.grid-2 {
  grid-column-start: 3;
  grid-column-end: 5;
  grid-row: 1;
  @media screen and (max-width: 60em) {
    grid-column-start: 1;
    grid-column-end: 5;
    grid-row: 2;
  }
}

.grid-3 {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row: 2;
  @media screen and (max-width: 60em) {
    grid-column-start: 1;
    grid-column-end: 5;
    grid-row: 3;
  }
}

.grid-4 {
  grid-column-start: 3;
  grid-column-end: 5;
  grid-row: 2;
  @media screen and (max-width: 60em) {
    grid-column-start: 1;
    grid-column-end: 5;
    grid-row: 4;
  }
}

</style>
<script>
  
export default {
    name: 'Resume',
    data: () => {
        return {
            hideResume: true,
            hideSkills: false
        }
    },
    methods: {
      showResume() {
        this.hideResume = false;
        this.hideSkills = true;
    }
  }
}
</script>