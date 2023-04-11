<template>
  <div class="about__container px-5 xl:px-0 pb-20 md:py-20 w-full h-full flex flex-col md:flex-row items-center gap-5 lg:gap-20">
    <div class="shadow__cards p-10 w-full md:w-1/2 h-1/2 md:h-full rounded-2xl" style="background-color: var(--negro);">
      <template class=" h-full" v-for="job in jobs" :key="job.id">
        <Info v-if="selected === job.id">
          <template #title>{{ job.title }}</template>
          <template #subtitle>{{ job.subtitle }}</template>
          <template #description>{{ job.description }}</template>
          <template #skills><strong>Skills: </strong>{{ job.skills }}</template>
        </Info>
      </template>
    </div>

    <div class="shadow__cards bg-blanco w-full md:w-1/2 h-1/2 md:h-full rounded-2xl relative">
      <div class="w-full flex justify-center items-center top-4 md:top-3/4 md:-bottom-16 absolute gap-4">
        <template v-for="n in 4">
          <button @click="setJob(n)" class="py-1 px-3 font-bold text-negro bg-negro bg-opacity-20 shadow-lg rounded-lg transition-all transform hover:scale-125">{{ n }}</button>
        </template>
      </div>
    </div>
  </div>
</template>

<script setup>


const selected = ref(1)
const jobs = ref([
  {
    id: 1,
    title: 'HelpCreaciones SAS' ,
    subtitle: 'Frontend Developer',
    description: 'Me desempeño en el desarrollo frontend de una PWA encargada de mantener en orden el inventario de las polizas de todo tipo para el cliente y el dashboard que administra la data de la web junto con el equipo de desarrollo',
    skills: 'Vue.js · Desarrollo Front-end · JavaScript · Git · Figma · Tailwind · Hojas de estilos en cascada (CSS) · HTML5 - Supabase'
  },
  {
    id: 2,
    title: 'Datain' ,
    subtitle: 'Frontend Developer',
    description: 'Se realizó diseño IU, desarrollo web de la landing page, desarrollo frontend y backend de dashboard para un cliente de la empresa.',
    skills: 'Vue.js · Desarrollo Front-end · JavaScript · Git · Figma · Tailwind · Node.js · Diseño web · Hojas de estilos en cascada (CSS) · HTML5 · Diseño de la interfaz de usuario'
  },
  {
    id: 3,
    title: 'Nodoland' ,
    subtitle: 'Frontend Developer',
    description: 'Se realizó un desarrollo frontend en la landing page y dashboard con la metodologia agil SCRUM',
    skills: 'Cypress.io · Vue.js · Desarrollo Front-end · JavaScript · Git · Figma · Tailwind · Hojas de estilos en cascada (CSS) · HTML5'
  },
  {
    id: 4,
    title: 'Frutos del Campo CTA' ,
    subtitle: 'Frontend Developer',
    description: 'Se realizó diseño IU y desarrollo web de la landing page.',
    skills: 'Vue.js · Desarrollo Front-end · JavaScript · Git · Figma · Diseño web · Hojas de estilos en cascada (CSS) · HTML5 · Diseño de la interfaz de usuario · Bootstrap'
  },
])

function setJob(index) {
  selected.value = index
  
}

</script>

<style>
  .card__img{
    background-color: #ffffff;
    /* background-image: url(../../assets/foto.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover; */
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