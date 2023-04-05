<template >
  <div class="h-full flex flex-col justify-center gap-2">
    <p class="texto text-2xl lg:text-4xl font-bold text-blanco">
      <slot name="title" ></slot>
    </p>
    <p class="texto mb-5 text-lg lg:text-xl text-blanco">
      <slot name="subtitle" ></slot>
    </p>
    <p class="texto mb-5 text-sm lg:text-base text-blanco">
      <slot name="description" ></slot>
    </p>
    <p class="texto text-sm lg:text-base  text-blanco">
      <slot name="skills" ></slot>
    </p>
  </div>
</template>

<style>
  .texto{
    transition: all .3s linear;
    animation: aparecer 2s ease .1s 1 both;
  }

  .texto ::backdrop{
    color: blue;
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