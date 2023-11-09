<script>
  let diceNumber = 0;
  const rollDice = () => {
    diceNumber = Math.floor(Math.random() * 6) + 1;
  };

</script>

<html lang="en">
    <button on:click={rollDice}>Roll The Dice</button>
    <p>The first dice rolled {diceNumber}</p>
</html>

<style></style>
