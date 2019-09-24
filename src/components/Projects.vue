<template>
    <section id='projects'>
        <div class='projects-container'>
            <div class='grid-item a'>
                <button class='see-more a' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor.png'/>
            </div>
            <div class='grid-item b'>
                <button class='see-more b' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ipreview.png'/>
            </div>
            <div class='grid-item c'>
                <button class='see-more c' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ransom-asanas.png'/>
            </div>
            <div class='grid-item d'>
                <button class='see-more d' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/better-calculator.png'/>
            </div>
            <div class='grid-item e'>
                <button class='see-more e' type='button'>View project</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/freeshelf.png'/>
            </div>
        </div>
    </section>
</template>

<script>
import Nav from "./Nav";

export default {
  name: 'Projects',
  components: {
    Nav
  }
}
</script>