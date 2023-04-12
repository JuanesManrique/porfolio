<template>
  <div class="main__container py-5 m-auto min-h-full grid">
    <!-- <div v-for="(project, index) in projects" :key="index" class="project w-full rounded-3xl relative">
      <video :ref="`video_${project.name}`" @mouseleave="pauseVideo(project.)" @mouseover="playVideo(project.)" class="project__video" muted loop playsinline preload="metadata" src="../../assets/video-portafolio.mp4" poster="../../assets/foto-portafolio.png"></video>
      <p class="project__title">{{project.name.charAt(0).toUpperCase() + project.name.slice(1)}}</p>
    </div> -->
    <div class="project w-full rounded-3xl relative">
      <video ref="video1" @mouseleave="pauseVideo(video1)" @mouseover="playVideo(video1)" class="project__video" muted loop playsinline preload="metadata" src="../../assets/video-portafolio.mp4" poster="../../assets/foto-portafolio.png"></video>
      <p class="project__title">Portafolio</p>
    </div>
    <div class="project w-full rounded-3xl relative">
      <video ref="video2" @mouseleave="pauseVideo(video2)" @mouseover="playVideo(video2)" class="project__video" muted loop playsinline preload="metadata" src="../../assets/video-talk2learn.mp4" poster="../../assets/foto-talk2learn.png"></video>
      <p class="project__title">Talk2learn <br><strong>(landing page)</strong></p>
    </div>
    <div class="project w-full rounded-3xl relative">
      <video ref="video3" @mouseleave="pauseVideo(video3)" @mouseover="playVideo(video3)" class="project__video" muted loop playsinline preload="metadata" src="../../assets/video-datain.mp4" poster="../../assets/foto-datain.png"></video>
      <p class="project__title">Datain <br><strong>(landing page)</strong></p>
    </div>
    <div class="project w-full rounded-3xl relative">
      <video ref="video4" @mouseleave="pauseVideo(video4)" @mouseover="playVideo(video4)" class="project__video" muted loop playsinline preload="metadata" src="../../assets/video-frutosdelcampo.mp4" poster="../../assets/foto-frutosdelcampo.png"></video>
      <p class="project__title">Frutos del Campo <br><strong>(landing page)</strong></p>
    </div>
    <div class="hidden md:block w-full rounded-3xl relative">
      <video class="opacity-0" preload="metadata" src="../../assets/video-portafolio.mp4"></video>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const video1 = ref()
const video2 = ref()
const video3 = ref()
const video4 = ref()
const autoplay = ref(false)

const projects = ref([
  {
    name:'portafolio',
    url: 'https://porfolio-juanesmanrique.vercel.app',
    video_portafolio: null
  },
 /*  {
    name:'talk2learn',
    url: 'https://porfolio-juanesmanrique.vercel.app'
  }, */
])

function playVideo(v) {
  v.play()
  /* console.log(v); */
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
    font-size: 40px;
    font-weight: 900;
    text-align: center;
    font-style: italic;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-shadow: 0 0 1em #000;
    z-index: 3;
    pointer-events: none;
  }

  @media (max-width: 600px) {
    .project__title{
      font-size: 30px;
    }
  }
</style>