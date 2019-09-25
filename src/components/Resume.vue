<template>
    <section 
    data-aos="fade-right"
    id='resume' class='home'>
        <!-- <div class='skill-grid'>
            <div class='grid-1'>
                <ul class='title'>Frameworks</ul>
                    <li class='intro'>Vue</li>
                    <li class='intro'>React</li>
                    <li class='intro'>Django</li>
                    <li class='intro'>SCSS</li>
            </div>
            <div class='grid-2'>
                <ul class='title'>Languages</ul>
                    <li class='intro'>JavaScript</li>
                    <li class='intro'>Python</li>
                    <li class='intro'>HTML</li>
                    <li class='intro'>CSS</li>
            </div>
            <div class='grid-3'>
                <ul class='title'>Databases</ul>
                    <li class='intro'>PostgreSQL</li>
                    <li class='intro'>SQLite</li>
            </div>

            <div class='grid-4'>
                <ul class='title'>Hosting</ul>
                    <li class='intro'>AWS S3</li>
                    <li class='intro'>Heroku</li>
                    <li class='intro'>Surge</li>
            </div>
        </div> -->

            <!-- <div class='grid-1'>
                <button class='see-more wht' role='button'>View resume</button>
            </div> -->
        <object class='resume' data='https://bean-project-screenshots.s3.amazonaws.com/bkoval-resume-21-9.pdf'></object>
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