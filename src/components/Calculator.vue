<template>
    <section class='indiv-proj-container'>
        <h2 class='proj-title b'>Calculator</h2>
        <div class='wrapper'>
            <table class='calc-table'>
                <th>
                <label class='all-access' for='calculator-input'>Either type numbers and operators, or use the buttons to make calculations</label>
                <td><input
                id='calculator-input'
                name='calculator-input'
                v-on:keyup.enter='evaluateInput()'
                class='display-box' 
                type='text'
                autofocus></td>
                </th>
                <tr class='table-row'>
                    <td><button id='operator' class='calc-button show-input'>(</button></td>
                    <td><button id='operator' class='calc-button show-input'>)</button></td>
                    <td><button id='operator' class='calc-button show-input'>%</button></td>
                    <td><button 
                    id='operator' 
                    class='calc-button'
                    @click='clearBox()'>C</button></td>
                </tr>
                <tr class='table-row'>
                <td><button class='calc-button show-input'>7</button></td>
                <td><button class='calc-button show-input'>8</button></td>
                <td><button class='calc-button show-input'>9</button></td>
                <td><button id='operator' class='calc-button show-input' aria-label='Add'>+</button></td>
                </tr>
                <tr class='table-row'>
                <td><button class='calc-button show-input'>4</button></td>
                <td><button class='calc-button show-input'>5</button></td>
                <td><button class='calc-button show-input'>6</button></td>
                <td><button id='operator' class='calc-button show-input' aria-label='Subtract'>-</button></td>
                </tr>
                <tr class='table-row'>
                <td><button class='calc-button show-input'>1</button></td>
                <td><button class='calc-button show-input'>2</button></td>
                <td><button class='calc-button show-input'>3</button></td>
                <td><button id='operator' class='calc-button show-input' aria-label='Multiply'>*</button></td>
                </tr>
                <tr class='table-row'>
                <td><button class='calc-button show-input'>0</button></td>
                <td><button class='calc-button show-input'>.</button></td>
                <td><button id='operator equal' 
                class='calc-button' 
                aria-label='Equal'
                @click='evaluateInput()'>=</button></td>
                <td><button id='operator' class='calc-button show-input' aria-label='Divide'>/</button></td>
                </tr>
            </table>
        </div>

        <div class='link-container'>
          <a class='links' target='blank' rel='noopener' href='https://github.com/bennykoval/portfolio-million/blob/master/src/components/Calculator.vue'>Source code</a>
        </div>

        <div class='more-info'>
          <h3 class='proj-info'>Above is a quick calculator which I initially built in <span class='tech a'>vanilla JavaScript, </span> then reworked into a <span class='tech b'>Vue component,</span> which means you can make calculations right on this page. Don't be shy - click some buttons!</h3>
        </div>
    </section>
</template>

<style lang='scss'>
$lb: #3383b5;
$lbs: #246d9b;
$db: #086199;
$dbs: #055080;


.wrapper {
    display: flex;
    // align-items: center;
    flex-flow: column wrap;
    width: 30vw;
    height: 80%;
    margin: auto;
    // justify-content: center;
  
    position: relative;
  
    $border: 5px;
    background-color: #d1d8e3;
    background-clip: padding-box; 
    border: solid $border transparent; 
    border-radius: 1em;
  
    &:before {
      content: '';
      position: absolute;
      top: 0; right: 0; bottom: 0; left: 0;
      z-index: -1;
      margin: -$border; 
      border-radius: inherit; 
      background: linear-gradient(to right, $lb, $dbs);
    }
  }


.calc-table {
    // width: 50vw;
    // margin: auto;
    display: grid;
    // grid-row-gap: 5%;
    // grid-column-gap: 10%;
    justify-items: center;
}

.table-row {
  display: flex;
}

td {
  margin: auto;
  padding: 3vh;
}

.display-box {
    text-align: right;
    font-family: sans-serif;
    font-size: 3rem;
    height: 3rem;
    width: 25vw;
    // margin: auto;
    border: none;
    border-bottom: 1.5px solid $db;
    background: linear-gradient(to right, $lb, $dbs);
    color: #FFF;
    text-shadow: 0px 4px 3px rgba(0,0,0,0.6),
    0px 8px 13px rgba(0,0,0,0.2),
    0px 18px 23px rgba(0,0,0,0.2);
}

#operator {
    background: $db;
    box-shadow: inset 0 -5px 0 0 $dbs;
    &:active {
      transform: translateY(3px);
      box-shadow: inset 0 -3px 0 0 $dbs;
      transition: 0.2 ease all;
    }
}

.calc-button {
    border-radius: 50%;
    color: rgba(255, 255, 255, 0.8);
    text-align: center;
    outline: none;
    font-size: 1rem;
    background: $lb;
    text-shadow: 0px 4px 3px rgba(0,0,0,0.6),
    0px 8px 13px rgba(0,0,0,0.2),
    0px 18px 23px rgba(0,0,0,0.2);
    width: 50px;
    height: 50px;
    box-shadow: inset 0 -5px 0 0 $lbs;
    &:active:not(#operator) {
      transform: translateY(3px);
      box-shadow: inset 0 -3px 0 0 $lbs;
    }
}

@media (max-width: 768px) and (orientation: portrait) {
    #calc-head {
        margin-top: 8%;
  }
    .wrapper {
        width: auto;
  }

    .calc-table {
        width: 50%;
  }

  .display-box {
        width: 55vw;
  }

  td {
        padding: .5vh;
  }

}
</style>

<script>
export default {
  name: 'Calculator',
  mounted() {
   const displayBox = document.querySelector('.display-box')
   this.displayStuff(displayBox).focus();
  },
  methods: {
    displayStuff(display) {
        let allNumButtons = document.querySelectorAll('.show-input');  
        for (let individualButton of allNumButtons) {
            individualButton.addEventListener('click', function () {
                    display.value += individualButton.innerText;
                    display.focus();
            })
          }
       },
    evaluateInput() {
        let displayBox = document.querySelector('.display-box');  
        displayBox.value = math.evaluate(displayBox.value);
        displayBox.focus();
    },
    clearBox() { 
        let displayBox = document.querySelector('.display-box');  
        displayBox.value = '';
        displayBox.focus();
    },
  }
};
</script>