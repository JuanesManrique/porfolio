<template>
  <div class="pt-5 w-full">
    <div class="shadow__cards px-10 w-full h-20 flex justify-between items-center shadow shadow-blanco-2 rounded-2xl" style="background-color: var(--negro);">
      <img src="../../assets/LOGO-05.png" alt="logo" class="h-10 opacity-80">
      <ul class="flex text-sm gap-10 font-black">
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link to="/">HOME</nuxt-link>
        </li>
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link to="/about">ABOUT</nuxt-link>
        </li>
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">PROJECTS</li>
        <li class=" opacity-80 cursor-pointer transition-all hover:opacity-100 hover:scale-105">
          <nuxt-link to="/jobs">JOBS</nuxt-link>
        </li>
      </ul>
    </div>  
  </div>
</template>
<style>
  .shadow__cards{
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;;
  }
</style>