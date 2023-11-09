<script>
  let diceNumber = "";
  function rollDice() {
    diceNumber = "";
    for (let i=0; i < 5; i++) {
      let roll = Math.floor(Math.random() * 6) + 1;
      diceNumber += roll.toString();
    }
    diceNumber = Number(diceNumber).toString();
  };


</script>

<html lang="en">
  <button on:click={rollDice}>roll the dice</button>
  <p>{diceNumber}</p>
</html>