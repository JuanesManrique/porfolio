<template>
  <div class="main__container py-5 m-auto min-h-full grid">
    <div class="project w-full rounded-3xl relative">
      <video ref="video" @mouseleave="pauseVideo(video)" @mouseover="playVideo(video)" class="project__video" muted playsinline preload="metadata" src="../../assets/video.mp4"></video>
      <p class="project__title">Portafolio</p>
    </div>
    <div class="w-full rounded-3xl relative ">
      <video class="opacity-0" preload="metadata" src="../../assets/video.mp4"></video>
    </div>
    <div class="hidden md:block w-full rounded-3xl relative">
      <video class="opacity-0" preload="metadata" src="../../assets/video.mp4"></video>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const video = ref()
const autoplay = ref(false)

const projects = ref([
  {
    id: 1,
    name:'Portafolio',
    url: 'https://porfolio-juanesmanrique.vercel.app'
  }
])

function playVideo(v) {
  v.play()
}

function pauseVideo(v) {
  v.pause()
}

</script>

<style>
  .main__container{
    width: calc(100% - 2em);
    grid-template-columns: repeat(auto-fit,minmax(30em,1fr));
    grid-gap: 2em;
    gap: 2em;
  }

  @media (max-width: 540px) {
    .main__container{
      grid-template-columns: repeat(auto-fit,minmax(15em,1fr));
    }
  }

  .project{
    transition: all .3s linear;
    color: #e0e0e0;
    background: var(--negro);
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;;
    overflow: hidden;
    animation: aparecer .8s ease 1 both;
  }

  .project__video{
    width: 100%;
    height: 100%;
    position: relative;
    z-index: 1;
    opacity: .1;
    transform: scale(1.4);
    transition: all .5s ease;
    cursor: pointer;
  }

  .project__video:hover{
    transform: scale(1.1);
    opacity: 0.8;
  }

  .project__title{
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    font-size: clamp(1em,60vw,2.5em);
    font-weight: 900;
    text-align: center;
    font-style: italic;
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;
    text-shadow: 0 0 1em #000;
    z-index: 3;
    pointer-events: none;
  }
</style>