<template>
  <div class="container-geral-footer">
    <div class="box-logo-line">
      <img src="../assets/img/logo.png" alt="logotipo" />
      <div class="line"></div>
    </div>
    <div class="content-buttom-inicio">
      <div class="box-buttom">
        <a href="/#home"
          ><ion-icon class="icon-link-topo" name="chevron-up-outline"></ion-icon
        ></a>
        <h3 class="ir-ao-topo">Ir ao Topo</h3>
      </div>
    </div>
    <div class="box-links">
      <div class="links">
        <h2 class="color-link">Menu</h2>
        <a class="itens-links" href="/">Home</a>
        <a class="itens-links" href="/#about">QuemSou</a>
        <a class="itens-links" href="/#oquefaco">O Que Faço</a>
        <a class="itens-links" href="/#portfolio">Portfólio</a>
      </div>
      <div class="links-1">
        <h2 class="color-link">Redes Sociais</h2>
        <a class="itens-links" href="https://www.instagram.com/" target="_blank"
          >Instagram</a
        >
        <a
          class="itens-links"
          href="https://www.linkedin.com/in/caique-oliveira-front-end/"
          target="_blank"
          >Linkedin</a
        >
      </div>
      <div class="links">
        <h2 class="color-link">Conatos</h2>
        <a class="itens-links" href="">(11) 93800-1071</a>
        <a class="itens-links" href="mailto:caiqueocastro@gmail.com"
          >caiqueocastro@gmail.com</a
        >
      </div>
    </div>
  </div>
</template>
<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container-geral-footer {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
  padding: 20px 0;
}
:root {
  --gradient: linear-gradient(to right, #e60303, #5b1325);
}
.content-buttom-inicio {
  display: flex;
  justify-content: center;
  align-items: baseline;
  width: 100%;
  padding-bottom: 50px;
}
.box-buttom {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.icon-link-topo {
  width: 70px;
  height: 70px;
  color: #5b1325;
}
.icon-link-topo:hover {
  border: 1px solid #5b1325;
}
.ir-ao-topo {
  color: #5b1325;
}
.box-logo-line {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 0 100px;
}
.line {
  width: 100%;
  border: 2px solid grey;
}
.box-links {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 100%;
  gap: 20px;
  padding-bottom: 50px;
}
.links {
  display: flex;
  justify-content: baseline;
  align-items: center;
  flex-direction: column;
  width: 250px;
  gap: 10px;
}
.links-1 {
  display: flex;
  justify-content: baseline;
  align-items: center;
  flex-direction: column;
  width: 250px;
  gap: 10px;
  border-left: 1px solid grey;
  border-right: 1px solid grey;
}
.color-link {
  color: red;
}
.itens-links {
  color: grey;
  text-decoration: none;
}
.itens-links:hover {
  color: red;
}

@media screen and (max-width: 786px) {
  .links-1 {
    border-left: none;
    border-right: none;
    border-top: 1px solid grey !important;
    border-bottom: 1px solid grey;
    padding: 20px 0;
  }
}
</style>
