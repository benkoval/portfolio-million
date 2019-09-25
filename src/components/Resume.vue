<template>
    <section id='resume' class='home'>
        <div class='skill-grid'>
            <ul class='title'>Frameworks</ul>
                <li class='intro'>Vue</li>
                <li class='intro'>React</li>
                <li class='intro'>Django</li>
                <li class='intro'>SCSS</li>
        </div>

        <div class='skill-grid'>
            <button class='see-more wht' role='button'>View resume</button>
        </div>
        <div class='skill-grid'>
            <ul class='title'>Languages</ul>
                <li class='intro'>JavaScript</li>
                <li class='intro'>Python</li>
                <li class='intro'>HTML</li>
                <li class='intro'>CSS</li>
        </div>

        <!-- <div class='skill-grid'>
            <ul class='title'>Version Control</ul>
                <li class='intro'>Git</li>
                <li class='intro'>GitHub</li>
        </div>

        <div class='skill-grid'>
            <ul class='title'>Databases</ul>
                <li class='intro'>PostgreSQL</li>
                <li class='intro'>SQLite</li>
        </div> -->


        <!-- <object class='resume' data='https://bean-project-screenshots.s3.amazonaws.com/bkoval-resume-21-9.pdf'></object> -->
    </section>
</template>

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