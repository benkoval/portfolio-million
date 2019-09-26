<template>
    <section 
    id='skills'
    class='skills-container'>
    <div class='empty'></div>
      <ul class='proj-intro'>Skills</ul>
          <div class='list-container'>
            <li 
            data-aos="zoom-in-right"
            class='li-skill d'>Django</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill a'>React</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill b'>HTML</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill c'>SCSS</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill c'>JavaScript</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill b'>Python</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill a'>GitHub</li>
            <li
            data-aos="zoom-in-right"
            class='li-skill d'>Vue</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill d'>Postgres</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill a'>Heroku</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill b'>AWS S3</li>
            <li 
            data-aos="zoom-in-right"
            class='li-skill c'>Surge</li>
          </div>
    <div class='back-btn-container'>
      <h3
      data-aos="fade-right"
      data-aos-offset='-300'
      class='placeholder-res'>See more on my <a id='resume-link' target='blank' rel='noopener' href='https://drive.google.com/file/d/1nzBria8QRxXHfioUllVkoKp-bFq2hHue/view'>resume</a></h3>
    </div>

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