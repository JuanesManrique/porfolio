<template>
  <div class="about__container px-5 xl:px-0 md:py-20 w-full h-full flex flex-col md:flex-row items-center gap-10 lg:gap-20">
    <div class="shadow__cards p-10 w-full md:w-1/2 h-1/2 md:h-full  flex flex-col justify-center rounded-2xl" style="background-color: var(--negro);">
      <p class="mb-5 text-xl lg:text-3xl text-start font-black">Juan Esteban Sanchez Manrique</p>
      <p class="mb-3 text-sm lg:text-lg">Soy un programador Front-end Developer con experiencia en desarrollos web con Vue.js empleando habilidades de estilos con tailwind, pruebas con Cypress.io, API REST y demas tecnologias complementarias al desarrollo front-end.</p>
      <p class="text-sm  lg:text-lg">Además de ser programador tambien entreno Capoeira, un arte marcial afro-brasileña en el cual llevo 11 años donde he participado en diversos eventos y campeonatos nacionales con el grupo Capoeira Nativos.</p>
    </div>
    <!-- <img src="../../assets/foto.jpg" alt="" class="shadow__cards img__about w-1/2 h-full rounded-2xl"> -->
    <div class="shadow__cards card__img w-full md:w-1/2 h-1/2 md:h-full rounded-2xl">
      <!-- <img src="../../assets/foto.jpg" alt="" class="shadow__cards w-1/2 h-full rounded-2xl"> -->
    </div>
  </div>
</template>

<script setup>


</script>

<style>
  .card__img{
    background-image: url(../../assets/foto.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
  }

  .shadow__cards{
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;;
  }
  .about__container{
    transition: all .3s linear;
    animation: aparecer 2s ease .6s 1 both;
  }

  @keyframes aparecer {
  0% {
    transform: translateY(1em);
    opacity: 0;
  }

  100% {
    transform: translateY(0);
    opacity: 1;
  }
}
</style>