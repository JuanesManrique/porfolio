<template>
  <div class="about__container py-20 w-full h-full flex justify-between items-center gap-20">
    <div class="shadow__cards p-10 w-1/2 h-full flex flex-col justify-center rounded-2xl" style="background-color: var(--negro);">
      
    </div>

    <div class="shadow__cards bg-blanco w-1/2 h-full rounded-2xl">
      <div class="w-full h-full flex justify-center items-end gap-4">
        <template v-for="n in 3">
          <button class="text-negro rounded-lg">{{ n }}</button>
        </template>
      </div>
    </div>
  </div>
</template>

<script setup>


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