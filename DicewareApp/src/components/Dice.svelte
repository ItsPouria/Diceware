<script>
  let diceNumber = 0;
  function randomNumber() {
        diceNumber = (Math.floor(Math.random() * 6) + 1);
        return diceNumber;
    }

</script>
<html lang="en">
        <button class="dice" on:click={randomNumber} aria-label="Roll dice">
          <div class="side one"></div>
          <div class="side two"></div>
          <div class="side three"></div>
          <div class="side four"></div>
          <div class="side five"></div>
          <div class="side six"></div>
        </button>

      <p>{diceNumber}</p>

</html>

<style>
.dice {
  position: relative;
  width: 200px;
  height: 200px;
 transform-style: preserve-3d;
  transform: rotateY(185deg) rotateX(150deg) rotateZ(315deg);
  animation: rotate 5s linear infinite;
}
.side {
  width: 100%;
  height: 100%;
  background: #da0060;
  border: 2px solid black;
  position: absolute;
  opacity: 0.7;
  display: flex;
  align-items: center;
  justify-content: center;
  &:before {
    content: "";
    width: 20%;
    height: 20%;
    background: black;
    border-radius: 50%;
  }
}
.base {
  width: 100%;
  height: 100%;
  transform: translateY(73px) rotateX(90deg);
    border: 0;
    background: blue;
}
.one {
    transform: translateZ(100px);
}
.two {
    transform: translateX(-100px) rotateY(-90deg);
  &:before {
    background: transparent;
    box-shadow: 
      #000 -50px -50px 0px 0px, 
      #000 50px 50px 0px 0px;
  }
}
.three {
    transform: translateY(100px) rotateX(90deg);
  &:before {
    box-shadow: 
      #000 -50px 50px 0px 0px, 
      #000 50px -50px 0px 0px;
  }
}
.four {
    transform: translateY(-100px) rotateX(90deg);
  &:before {
    background: transparent;
    box-shadow: 
      #000 -50px 50px 0px 0px, 
      #000 -50px -50px 0px 0px,
      #000 50px 50px 0px 0px, 
      #000 50px -50px 0px 0px;
  }
}
.five {
    transform: translateX(100px) rotateY(90deg);
  &:before {
    box-shadow: 
      #000 -50px -50px 0px 0px, 
      #000 -50px 50px 0px 0px,
      #000 50px -50px 0px 0px, 
      #000 50px 50px 0px 0px;
  }
}
.six {
    transform: translateZ(-100px);
  &:before {
    background: transparent;
    box-shadow: 
      #000 -50px -50px 0px 0px, 
      #000 -50px 0px 0px 0px,
      #000 -50px 50px 0px 0px, 
      #000 50px -50px 0px 0px, 
      #000 50px 0px 0px 0px,
      #000 50px 50px 0px 0px;
  }
}



@keyframes rotate {
  from {
    transform: rotateY(0) rotateX(30deg) rotateZ(30deg);
  }
  to {
    transform: rotateY(360deg) rotateX(30deg) rotateZ(30deg);
  }
}
</style>