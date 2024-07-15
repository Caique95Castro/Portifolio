<template>
  <div class="container-geral-servico">
    <div class="box-content">
      <div class="line-1"></div>
      <div class="name-title">
        <h1 class="titulo">O que Faço</h1>
        <p class="sub-titulo">SERVIÇOS E SOLUÇÕES</p>
      </div>
      <div class="line-1"></div>
    </div>
    <div class="container-servicos">
      <div class="box-content-servicos">
        <div class="box-servicos" id="box-servicos">
          <img src="../assets/img/web.png" alt="" class="image-servico" />
          <p class="text-servico"><strong>Desenvolvimento Web</strong></p>
          <p class="text-servico">
            Como desenvolvedor web, transformo ideias em experiências digitais
            interativas e funcionais, sites responsivos e dinamocos.
          </p>
          <a href="" class="link-contato"
            ><button class="link-contato">Saiba mais</button></a
          >
        </div>
        <div class="box-servicos" id="box-servicos-1">
          <img
            src="../assets/img/app-play.png"
            alt=""
            class="image-servico-1"
          />
          <p class="text-servico">
            <strong>Desenvolvimento de Aplicativos Móveis</strong>
          </p>
          <p class="text-servico">
            Como desenvolvedor iniciante em aplicativos móveis, estou começando
            a transformar ideias em aplicativos funcionais para iOS e Android
            usando Flutter, Dart como linguagem, Android Studio, Kotlin e Java.
          </p>
          <a href="" class="link-contato"
            ><button class="link-contato">Saiba mais</button></a
          >
        </div>
      </div>
    </div>
    <div class="box-content-line">
      <img src="../assets/img/linha-meio.png" alt="" class="line-meio" />
    </div>
  </div>
</template>
<script>
import ScrollReveal from "scrollreveal";

export default {
  mounted() {
    const sr = ScrollReveal({
      duration: 4000,
      distance: "10rem",
      reset: true,
    });

    sr.reveal("#box-servicos", { origin: "top", scale: 0.9 });
    sr.reveal("#box-servicos-1", { origin: "bottom", scale: 0.9 });
  },
};
</script>
<style src="./css/OqueFaco.css" scoped></style>
