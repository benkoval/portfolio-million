<template>
    <section class='indiv-proj-container'>
        <div id='pokemon'>
            <h1 class='pkmn-title' v-if='silhouette'>Who's that Pokémon?</h1>
            <div 
            v-if="!silhouette"
            class='failDiv'>
                <h1 class='pkmn-title'>It's <span class='uppercase'>{{frontName}}!</span></h1>
            </div>
            <img 
            class='img'
            :class="{ silhouette: silhouette }"
            :src="frontSprite"/>

          <form
          class="input-container" 
          id="guess-form" 
          onsubmit="return false">
            <label class="all-access" for="guess-field">Type your guess here.</label>
            <input
            v-model='userGuess'
            id="guess-field" 
            class="guess-input" 
            name="guess-field" 
            type="search" 
            placeholder="Guess"/>
            <button
            class='uppercase'
            @click.prevent='correctOrNah(userGuess)'
            id="guess-button"
            type="submit"><span class="all-access">Submit your guess</span><img class='pokeball' src='https://image.flaticon.com/icons/svg/361/361998.svg'></button>
          <div class='surrenderContainer'>
            <button
            @click.prevent='displaySpriteName()'
            type='submit'
            class='surrenderButton'>
            I give up!
            </button>
          </div>
        </form>

            <div 
            v-if="incorrectGuess"
            class='failDiv'>
            <h2 class='pkmn-title'>Guess again!</h2>
            </div>
        </div>
        <div class='link-container'>
          <a class='links' target='blank' rel='noopener' href='https://github.com/bennykoval/portfolio-million/blob/master/src/components/Pokemon.vue'>Source code</a>
        </div>

        <div class='more-info'>
          <h3 class='proj-info'>"Who's That Pokemon?" pays homage to my childhood. I built this cute little game with <span class='tech d'>Vue, </span> and I used <span class='tech d'>Axios </span> to access data from the Poke API.</h3>
        </div>
    </section>
</template>


<style lang='scss'>

@import url('https://fonts.googleapis.com/css?family=Press+Start+2P&display=swap');
@import url('https://fonts.googleapis.com/css?family=VT323');
$gameFont: 'Press Start 2P', cursive;
$btnFont: 'VT323', monospace;

#pokemon {
  text-align: center;
}

.pkmn-title {
  font-family: $btnFont;
  font-size: 3rem;
  color: #FF6F61;
}
.surrenderButton {
  font-family: $btnFont;
	background: #881400;
	border-bottom: 5px inset rgba(0,0,0,.5);
	border-left: 5px inset rgba(0,0,0,.5);
	border-right: 5px inset rgba(255,255,255,.5);
	border-top: 5px inset rgba(255,255,255,.5);
	box-sizing: border-box;
	color: white;
	cursor: pointer;
	font-size: 1.8rem;
	margin: auto;
	min-width: 150px;
	padding: .3rem;
	text-transform: uppercase;
	
	&:focus,
	&:hover {
		background: #A81000;
	}
}

.surrenderContainer {
  display: flex;
}
.uppercase {
  text-transform: uppercase;
  margin-bottom: 40px;
  border: none;
  cursor: pointer;
}
// .img {
//   height: 40vh;
// }
.silhouette {
    filter: contrast(0) brightness(0);
    pointer-events: none;
}

.failText {
  font-size: 6rem;
  color: #000;
}

.pokeball {
  height: 2.2vh;
  width: 2.2vw;
}

</style>

<script>
import axios from "axios";

export default {
  name: 'Pokemon',
  data () {
      return {
          frontSprite: '',
          frontName: '',
          userGuess: '',
          randomInt: 0,
          incorrectGuess: false,
          silhouette: true,
          min: 1,
          max: 151
      }
  },
  mounted() {
    this.getFrontSprite();
  },
  methods: { 
      getFrontSprite() {
        let randInt = Math.floor(Math.random() * (this.max - this.min + 1) + this.min);
        axios
        .get(`https://pokeapi.co/api/v2/pokemon/${randInt}/`)
        .then(response =>
            (this.frontName = response.data.name.replace(/\-.*/, ''),
            this.frontSprite = response.data.sprites.front_default));
        this.silhouette = true;
      },
      clearInput() {
        this.userGuess = '';
      },
      correctOrNah(guess) {
        if (guess.toLowerCase() != this.frontName) {
          this.incorrectGuess = true
        }
        else {
          this.displaySpriteName();
        }
        this.clearInput();
      },
      displaySpriteName() {
        this.incorrectGuess = false
        this.silhouette = false
        setTimeout(() => this.getFrontSprite(), 2000);
      }
  }
}
</script>