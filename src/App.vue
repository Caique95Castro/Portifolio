<template>
  <section class="module parallax parallax-2">
    <a href="#home" id="home"></a>
    <div class="container-geral-header">
      <div class="content-logo-1">
        <img class="img-logo" src="./assets/img/logo.png" alt="" />
      </div>

      <button class="hamburger" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>
      <nav :class="{ open: isOpen }" id="menu-desktop">
        <router-link class="links-menu" to="/" @click="closeMenu"
          >Home</router-link
        >
        <a class="links-menu" href="/#about" @click="closeMenu">Quem Sou</a>
        <div class="content-logo">
          <img src="./assets/img/logo.png" alt="logo" />
        </div>
        <a class="links-menu" href="/#oquefaco" @click="closeMenu"> Que Faço</a>
        <a class="links-menu" href="/#portfolio" @click="closeMenu"
          >Portfólio</a
        >
      </nav>
    </div>
  </section>
  <div class="container-geral-header-1">
    <div class="content-logo-1">
      <img class="img-logo" src="./assets/img/logo.png" alt="" />
    </div>

    <button class="hamburger" @click="toggleMenu">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </button>
    <nav :class="{ open: isOpen }" id="menu-desktop">
      <router-link class="links-menu" to="/" @click="closeMenu"
        >Home</router-link
      >
      <a class="links-menu" href="/#about" @click="closeMenu">Quem Sou</a>
      <a class="links-menu" href="/#oquefaco" @click="closeMenu"> Que Faço</a>
      <a class="links-menu" href="/#portfolio" @click="closeMenu">Portfólio</a>
    </nav>
  </div>
  <router-view />
</template>
<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    closeMenu() {
      this.isOpen = false;
    },
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
:root {
  --gradient: linear-gradient(to right, #e60303, #5b1325);
}
body {
  background-color: #000;
}
section.module.parallax {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 450px;
  width: 100%;
  position: relative;
  overflow: hidden;
  border-bottom-left-radius: 300px;
  border-bottom-right-radius: 300px;
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}

@media screen and (max-width: 500px) {
  section.module.parallax {
    display: none;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 0 auto !important;
    width: 100%;
    position: relative;
    overflow: hidden;
    background-position: 50% 50%;
    background-repeat: no-repeat;
    background-attachment: scroll;
    background-size: cover;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
  }
}

section.module.parallax:after {
  content: "";
  height: 110%;
  width: 100%;
  position: absolute;
  z-index: 8;
  background: -webkit-linear-gradient(
    to bottom,
    rgba(10, 10, 10, 0.4) 40%,
    rgba(10, 10, 10, 0.4) 40%,
    #000 100%
  );
  background: -moz-linear-gradient(
    to bottom,
    rgba(10, 10, 10, 0.4) 40%,
    rgba(10, 10, 10, 0.4) 40%,
    #000 100%
  );
  background: -o-linear-gradient(
    to bottom,
    rgba(10, 10, 10, 0.4) 40%,
    rgba(10, 10, 10, 0.4) 40%,
    #000 100%
  );
  background: linear-gradient(
    to bottom,
    rgba(10, 10, 10, 0.4) 10%,
    rgba(10, 10, 10, 0.4) 10%,
    #000 100%
  );
}

section.module.parallax-2 {
  background-image: url(./assets/img/image-fundo-inicio.png);
}

.container-geral-header {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
  gap: 50px;
  width: 100%;
}
.container-geral-header-1 {
  display: none;
  justify-content: center;
  align-items: center;
  padding: 10px;
  gap: 50px;
  width: 100%;
  background-image: linear-gradient(140deg, #e60303 0%, #5b1325 100%);
}

.content-logo {
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 100;
  width: 300px;
}
.content-logo-1 {
  display: none;
}
.logo {
  width: 130px;
  height: 130px;
}

.hamburger {
  display: none;
  flex-direction: column;
  justify-content: space-around;
  width: 30px;
  height: 30px;
  background: transparent;
  border: none;
  cursor: pointer;
  z-index: 100;

  .bar {
    width: 100%;
    height: 4px;
    background-color: red;
    border-radius: 2px;
    transition: all 0.3s ease;
  }
}
.links-menu {
  font-size: 25px;
}
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  z-index: 100;

  &.open {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 80px;
    right: 0;
    background-color: #fff;
    width: 100%;
    height: auto;
  }

  a {
    font-weight: bold;
    color: rgb(129, 129, 129);
    text-decoration: none;

    &.router-link-exact-active {
      color: red;
    }
  }

  a:hover {
    color: red;
    text-decoration: none;
  }
}

@media (max-width: 768px) {
  .container-geral-header-1 {
    display: flex;
    justify-content: space-between !important;
    padding: 0 50px;
    background-image: linear-gradient(140deg, #e60303 0%, #5b1325 100%);
    z-index: 1000;
  }
  .content-logo {
    display: none;
  }
  .content-logo-1 {
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
    width: 150px;
    height: 100px;
  }
  .img-logo {
    width: 150px;
    height: 100px;
  }
  .hamburger {
    display: flex;
  }

  nav {
    display: none;

    &.open {
      display: flex;
      z-index: 1000;
      margin-top: 20px;
      padding: 20px 0;
      background-image: linear-gradient(140deg, #e60303 0%, #5b1325 100%);
    }
  }
}
</style>
