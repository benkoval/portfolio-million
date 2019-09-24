<template>
    <section id='projects'>
        <div class='projects-container'>
            <div class='grid-item'>
                <h3 class='title-proj'>decidOR</h3>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor.png'/>
                <p class='descrip-proj'>See more</p>
            </div>
            <div class='grid-item'>
                <h3 class='title-proj'>iPreview</h3>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ipreview.png'/>
                <p class='descrip-proj'>See more</p>
            </div>
            <div class='grid-item'>
                <h3 class='title-proj'>Random Asanas</h3>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ransom-asanas.png'/>
                <p class='descrip-proj'>See more</p>
            </div>
            <div class='grid-item'>
                <h3 class='title-proj'>Calculator</h3>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/better-calculator.png'/>
                <p class='descrip-proj'>See more</p>
            </div>
            <div class='grid-item'>
                <h3 class='title-proj'>Freeshelf</h3>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/freeshelf.png'/>
                <p class='descrip-proj'>See more</p>
            </div>
        </div>
    </section>
</template>

<style lang='scss'>
$lato: 'Lato', sans-serif;
$lex: 'Playfair Display', serif;

.projects-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(30vw, 4fr));
    grid-gap: 10px;
    // grid-auto-rows: minmax(180px, auto);
    grid-auto-flow: dense;
    padding: 10px;
}

.grid-item {
    margin: auto;
    padding: 1rem;
    color: #FFF;
    background-color: #7C59AF;
    border-radius: 5px;
    &:nth-child(odd) {
        background-color: #3A5BAC;
    }
}

.title-proj {
    text-align: center;
    font-family: $lex;
    letter-spacing: 1px;
    font-size: 2em;
    text-transform: uppercase;
}

.deck-img {
    margin: auto;
    width: 30vw;
    border-radius: 5px;
}

.descrip-proj {
    font-family: $lato;
    text-align: center;
    font-size: 1.1em;
    &:after {
        content: '';
        margin: 0 auto;
        display: block;
        width: 17%;
        border-bottom: .16vw solid;
        padding-bottom: .3rem;
    }
}
</style>