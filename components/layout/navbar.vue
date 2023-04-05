<template>
  <div class="pt-5 px-5 xl:px-0 w-full transition-all">
    <div class="header w-full h-full md:px-10 md:h-20 top-0 left-0 flex flex-col md:flex-row justify-center md:justify-between items-center rounded-3xl md:rounded-2xl fixed md:static" :class="classButton">
      <img src="../../assets/LOGO-05.png" alt="logo" class="mb-10 md:mb-0 h-20 md:h-10 opacity-80">
      <ul class="mb-20 md:mb-0 flex flex-col md:flex-row text-center text-lg md:text-sm gap-10 font-black">
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link @click="classButton = ''" to="/">HOME</nuxt-link>
        </li>
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link @click="classButton = ''" to="/about">ABOUT</nuxt-link>
        </li>
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link @click="classButton = ''" to="/projects">PROJECTS</nuxt-link>
        </li>
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link @click="classButton = ''" to="/jobs">JOBS</nuxt-link>
        </li>
      </ul>
      <div class="flex md:hidden gap-5">
        <a href="https://www.instagram.com/juanemanrique/" target="_blank">
          <Icon name="ion:logo-instagram" class="text-3xl"/>
        </a>
        <a href="https://github.com/JuanesManrique" target="_blank">
          <Icon name="mdi:github" class="text-3xl"/>
        </a>
        <a href="https://www.linkedin.com/in/juan-sanchezm" target="_blank">
          <Icon name="bi:linkedin" class="text-3xl"/>
        </a>
      </div>
    </div> 
    <div class="header" :class="classButton"></div>
    <button @click="toggleMenu" class="icon__menu md:hidden" :class="classButton"></button>
  </div>
</template>

<script setup>

const classButton = ref('')

const toggleMenu = () => {
  if (classButton.value == '') {
    classButton.value = 'active'
  } else {
    classButton.value = ''
  }
}

</script>

<style scoped>
  .header{
    background-color: var(--negro);
    color: #e0e0e0;
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;
    z-index: 3;
    transition: all .5s ease;
  }

  li p{
    display: none;
  }

  @media (max-width: 768px) {
    .header{
      opacity: 0;
      transform: scale(1.2);
      pointer-events: none;
    }

    li p{
    display: block;
  }
  }

  .header.active {
    opacity: 1;
    transform: scale(1);
    pointer-events: auto;
  }

  .icon__menu{
    width: 5em;
    height: 5em;
    cursor: pointer;
    position: fixed;
    bottom: 1em;
    right: 1em;
    z-index: 3;
    overflow: hidden;
    border-radius: 50%;
    background: var(--negro);
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;
  }

  .icon__menu::before{
    content: "";
    width: 50%;
    height: 0.2em;
    top: calc(60% - 0.1em);
    background-color: #e0e0e0;
    background-color: var(--blanco);
    display: block;
    position: absolute;
    left: 25%;
    transform: rotate(0deg);
    transition: all .3s ease;
  }

  .icon__menu.active::before{
    top: calc(50% - 0.1em);
    transform: rotate(-45deg);
  }

  .icon__menu::after{
    content: "";
    width: 50%;
    height: 0.2em;
    top: calc(40% - 0.1em);
    background-color: #e0e0e0;
    background-color: var(--blanco);
    display: block;
    position: absolute;
    left: 25%;
    transform: rotate(0deg);
    transition: all .3s ease; 
  }

  .icon__menu.active::after{
    top: calc(50% - 0.1em);
    transform: rotate(45deg);
  }
</style>