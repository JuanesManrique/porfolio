<template>
  <div class="about__container py-10 w-full h-full flex justify-between items-center gap-20">
    <div class="shadow__cards p-10 w-1/2 h-full flex flex-col justify-center rounded-2xl" style="background-color: var(--negro);">
      <p class="mb-5 text-3xl font-black">Juan Esteban Sanchez Manrique</p>
      <p class="mb-3 text-lg">Soy un programador Front-end Developer con experiencia en desarrollos web con el framework Vue.js empleando habilidades de estilos con tailwind, pruebas con Cypress.io, API REST y demas tecnologias complementarias al desarrollo front-end...</p>
      <p class="text-lg">Además de ser programador tambien entreno Capoeira, un arte marcial afro-brasileña en el cual llevo 11 años donde he participado en diversos eventos y campeonatos nacionales con el grupo Capoeira Nativos.</p>
    </div>
    <div class="shadow__cards w-1/2 h-full rounded-2xl" style="background-color: var(--negro);">
    </div>
  </div>
</template>

<script setup>


</script>

<style>
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