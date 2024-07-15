<template>
  <div class="container-geral-about">
    <div class="box-content-about">
      <div class="text-content" id="text-content">
        <p class="textos">
          Eleve o sucesso da sua empresa com um site profissional.
        </p>
        <p class="textos">
          Converta sua presença digital em uma poderosa ferramenta de geração de
          negócios com um site feito sob medida.
        </p>
      </div>
      <div class="img-content">
        <img class="image-image" src="../assets/img/image-1.png" alt="" />
      </div>
      <div class="text-content" id="text-content-1">
        <h1>Olá,</h1>
        <p class="textos">
          Sou Caique de Oliveira Castro, desenvolvedor web e mobile em constante
          aprendizado. Tenho 2 anos de experiência no desenvolvimento web, onde
          adquiri habilidades sólidas em criar sites dinâmicos e responsivos.
          Recentemente, comecei minha jornada no desenvolvimento mobile, com 3
          meses de dedicação e entusiasmo para expandir meu conhecimento nesta
          área.
        </p>
        <p class="textos">
          Atualmente, estou cursando Análise e Desenvolvimento de Sistemas, onde
          busco aprimorar minhas competências técnicas e acompanhar as
          tendências e inovações do setor. Estou sempre em busca de novos
          desafios e oportunidades para crescer como desenvolvedor e entregar
          soluções eficientes e criativas.
        </p>
      </div>
    </div>
    <div class="box-content-skils">
      <h2>MINHAS <span class="spans">HARD SKILLS</span></h2>

      <div class="container-content-carousel">
        <CarouselTemplate />
        <CarouselVue />
      </div>
    </div>
  </div>
</template>
<script>
import CarouselTemplate from "./CarouselTemplate.vue";
import CarouselVue from "./CarouselVue.vue";
import ScrollReveal from "scrollreveal";

export default {
  components: {
    CarouselTemplate,
    CarouselVue,
  },
  mounted() {
    const sr = ScrollReveal({
      duration: 4000,
      distance: "10rem",
      reset: true,
    });
    sr.reveal("#text-content", { origin: "top", scale: 0.9 });
    sr.reveal("#text-content-1", { origin: "bottom", scale: 0.9 });
  },
};
</script>
<style src="./css/About.css" scoped></style>
