<template>
  <div class="slider">
    <div class="slide-track">
      <div class="slide">
        <img src="../assets/img/development.png" alt="" />
      </div>
      <div class="slide">
        <img src="../assets/img/responsive.png" alt="" />
      </div>
      <div class="slide">
        <img src="../assets/img/clean.png" alt="" />
      </div>

      <div class="slide">
        <img src="../assets/img/development.png" alt="" />
      </div>
      <div class="slide">
        <img src="../assets/img/responsive.png" alt="" />
      </div>
      <div class="slide">
        <img src="../assets/img/clean.png" alt="" />
      </div>

      <div class="slide">
        <img src="../assets/img/development.png" alt="" />
      </div>
      <div class="slide">
        <img src="../assets/img/responsive.png" alt="" />
      </div>
      <div class="slide">
        <img src="../assets/img/clean.png" alt="" />
      </div>
    </div>
  </div>
</template>
  <script></script>
  <style scoped>
  body {
    min-height: 100vh;
    display: grid;
    place-items: center;
  }
  
  .slider {
    height: 500px;
    margin: auto;
    position: relative;
    width: 90%;
    display: grid;
    place-items: center;
    overflow: hidden;
  }
  
  .slide-track {
    display: flex;
    width: calc(500px * 9);
    animation: scroll 40s linear infinite;
  }
  
  .slide-track:hover {
    animation-play-state: paused;
  }
  
  @keyframes scroll {
    0% {
      transform: translateX(calc(-500px * 9));
    }
    100% {
      transform: translateX(0);
    }
  }
  
  .slide {
    height: 500px;
    width: 500px;
    display: flex;
    align-items: center;
    padding: 15px;
    perspective: 100px;
  }
  
  img {
    width: 100%;
    transition: transform 1s;
    border-radius: 20px;
  }
  
  img:hover {
    transform: translateZ(20px);
  }
  
  .slider::before,
  .slider::after {
    background: linear-gradient(
      to right, 
      rgba(255, 255, 255, 1) 0%, 
      rgba(255, 255, 255, 0)
    );
    content: "";
    height: 100%;
    position: absolute;
    width: 15%;
    z-index: 2;
  }
  
  .slider::before {
    left: 0;
    top: 0;
  }
  
  .slider::after {
    right: 0;
    top: 0;
    transform: rotate(180deg);
  }
  </style>
  