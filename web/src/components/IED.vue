<template>
  <div class="sdplus animate-float">
      <div class="logo-container">
        <img src="../assets/images/tt-logo.png" alt="" class="tt-logo" />
        <p class="sdplus-text">SD+</p>
      </div>
      <div class="display">
        <p class="display-text-1"></p>
        <p class="display-text-2"></p>
      </div>
      <div class="divider"></div>
      <div class="leds">
        <div class="led"></div>
        <div class="led"></div>
        <div class="led"></div>
        <div class="led"></div>
        <div class="led"></div>
        <div class="led"></div>
        <div class="led"></div>
        <div class="led"></div>
      </div>
      <div class="buttons">
        <button disabled type="button" class="button" id="p-button">P</button>
        <button disabled type="button" class="button" id="up-button">⇡</button>
        <button disabled type="button" class="button" id="down-button">⇣</button>
        <button disabled type="button" class="button" id="enter-button">⇠</button>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
@import "../assets/css/animations.css";

@media screen and (min-width: 1024px) {
.mobile {
  display: none;
}

.sdplus {
    position: absolute;
  
    display: flex;
    flex-direction: column;
    align-items: center;
  
    position: absolute;
    width: 90mm;
    height: 90mm;
  
    background: white;
  
    border: 0.8mm solid black;
  
    transform: rotate(10deg) skew(10deg) translate(0, 0);
    margin-top: 5rem;
    margin-right: 24rem;
  
    box-shadow: 0 4px 18px 0 black;
  }
  
  .sdplus:before {
    content: "";
    position: absolute;
    width: 65mm;
    height: 90.1mm;
    background: #181818;
    transform: skewY(-40deg) rotate(0deg);
    left: 89mm;
    top: -28.1mm;
  
    box-shadow: 7px 4px 18px 0 black;
  }
  
  .sdplus:after {
    content: "";
    position: absolute;
    width: 89.8mm;
    height: 54.7mm;
    background: #393939;
    transform: skewX(-50deg) rotate(0deg);
    left: 31.7mm;
    top: -55.4mm;
  }
  
  .sdplus:hover {
      animation-play-state: paused;
      zoom: 1.08;
  }
  
  .logo-container {
    position: relative;
    width: 75%;
    height: 17.5%;
  
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row;
  
    justify-self: flex-start;
  
    background: white;
  
    margin: 0.8rem 0;
  }
  
  .tt-logo {
    width: 45px;
    height: 45px;
  }
  
  .sdplus-text {
    font-family: "Orbitron", sans-serif;
    font-size: 2.5rem;
    font-weight: 800;
  }
  
  .display {
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: "Orbitron", sans-serif;
    font-weight: 500;
    font-size: 15px;
    text-transform: uppercase;
    text-align: center;
    flex-direction: column;
  
      box-shadow: inset 0 0 12px 0 black;
  
    position: relative;
    width: 75%;
    height: 1.7cm;
  
    background: #094b1e;
  }
  
  .display-text-1,
  .display-text-2 {
    position: relative;
    margin: .2rem;
    color: #7eff29;
    letter-spacing: 2px;
    line-height: 1.5;
  
    text-shadow: 0 0 4px #7eff29;
  }
  
  .divider {
    position: relative;
  
    width: 100%;
    height: 5%;
  
    margin-top: 3rem;
  
    background: #1c1c1c;
  }
  
  .leds {
    position: relative;
  
    margin-top: 1rem;
  
    align-items: center;
    justify-content: center;
  
    width: 100%;
    height: 5%;
  
    display: flex;
    flex-direction: row-reverse;
  }
  
  .led {
    padding-top: 1rem;
    background: darkred;
    width: 1rem;
    height: 1rem;
    border-radius: 50%;
    margin: 0 1.3rem;
  }
  
  .buttons {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
  
    width: 90%;
  }
  
  .button {
    background: white;
    border-radius: 50%;
  
    text-align: center;
  
    color: #5bb51e;
    font-family: "Orbitron", sans-serif;
    font-weight: 800;
    font-size: 18px;
  
    width: 38px;
    height: 38px;
    margin: 2.4rem 1.7rem;
  
    border: 1px solid #747474;
    box-shadow: inset 0 0 2px 0 black;
    box-shadow: 1px 1px 4px -1px black;
  
    outline: none;
    cursor: pointer;
  }
  
  .button:active {
    transform: translateY(0.5px);
    box-shadow: none;
  }

  .options {
    position: fixed;
    width: 100px;
    height: 400px;
    background: #2e4333;
    left: 4rem;
    top: auto;
    padding: 4rem 1rem;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;

    border-radius: 50px;
  }

  .on-off {
      display: flex;
      align-items: center;
      justify-content: center;

      width: 100%;
  }

  #on-off {
    position: absolute;
    opacity: 0;
    width: 0;
    height: 0;
  }

  .switch {
      width: 5rem;
      height: 5rem;
      cursor: pointer;
      opacity: .3;

      transition: 300ms;
  }

  #on-off:checked + .switch {
    opacity: 1;
  }
}

</style>