<script>
  import {wordlist} from './eff';
  let diceNumber = "";
  let word = "";
  function rollDice() {
    diceNumber = "";
    for (let i=0; i < 5; i++) {
      let roll = Math.floor(Math.random() * 6) + 1;
      diceNumber += roll.toString();
    }
    // @ts-ignore
    word = wordlist[(parseFloat(diceNumber))];
    
  };


</script>

<html lang="en">
  <button on:click={rollDice}>roll the dice</button>
  <p>{diceNumber}</p>
  <p> the chosen word is {word}</p>
</html>