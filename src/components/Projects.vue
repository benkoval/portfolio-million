<template>
    <section id='projects'>
        <div class='projects-container'>
            <div class='grid-item'>
                <div class='btn-container'>
                    <button class='see-more pulse' type='button'>See more</button>
                </div>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/decidor.png'/>
            </div>
            <div class='grid-item'>
                <button class='see-more' type='button'>See more</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ipreview.png'/>
            </div>
            <div class='grid-item'>
                <button class='see-more' type='button'>See more</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/ransom-asanas.png'/>
            </div>
            <div class='grid-item'>
                <button class='see-more' type='button'>See more</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/better-calculator.png'/>
            </div>
            <div class='grid-item'>
                <button class='see-more' type='button'>See more</button>
                <img class='deck-img' src='https://bean-project-screenshots.s3.amazonaws.com/freeshelf.png'/>
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

.btn-container {
    display: flex;
    justify-content: center;
}

.grid-item {
    position: relative;
    margin: auto;
    padding: 1rem;
    color: #FFF;
    background-color: #7C59AF;
    border-radius: 5px;
    &:nth-child(odd) {
        background-color: #3A5BAC;
    }
}

.see-more {
    position: absolute;
    z-index: 2;
    color: #fff;
    text-transform: uppercase;
    font-family: $lato;
    background: none;
    border: 2px solid;
    font: inherit;
    line-height: 1;
    margin: 0.5em;
    padding: 1em 2em;
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
    z-index: 1;
    position: relative;
    filter: brightness(40%) grayscale(20%);
}

// .overlay:before {
//     content: '';
//     z-index: 2;
//     border-radius: 5px;
//     width: 30vw;
//     height: 100%;
//     position: absolute;
//     display: inline-block;
//     background: linear-gradient(0deg, rgba(7, 41, 89, 0.8) 0%, 
//     rgba(7, 41, 89, 0.18) 36%, rgba(7, 41, 89, 0) 46%), 
//     // box-shadow: 0 20px 30px rgba(0,0,0,0.2);
// }

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

.pulse:hover, 
.pulse:focus-within {
  animation: pulse 1s;
  box-shadow: 0 0 0 2em rgba(#fff,0);
}

@keyframes pulse {
  0% { box-shadow: 0 0 0 0 var(--hover); }
}
</style>