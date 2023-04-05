<template>
  <div class="pb-5 px-5 xl:px-0 w-full transition-all">
    <div class="shadow__cards px-10 w-full h-20 hidden md:flex justify-between items-center rounded-2xl" style="background-color: var(--negro);">
      <p class="text-xl font-black opacity-80 uppercase">contact</p>
      <div class="flex gap-5">
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
  </div>
</template>
<style>
  .shadow__cards{
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;;
  }
</style>