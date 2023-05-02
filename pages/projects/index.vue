<template>
  <div class="main__container py-5 m-auto min-h-full grid">
    <!-- <div v-for="(project, index) in projects" :key="index" class="project w-full rounded-3xl relative">
      <video :ref="`video_${project.name}`" @mouseleave="pauseVideo(project.)" @mouseover="playVideo(project.)" class="project__video" muted loop playsinline preload="metadata" src="../../assets/video-portafolio.mp4" poster="../../assets/foto-portafolio.png"></video>
      <p class="project__title">{{project.name.charAt(0).toUpperCase() + project.name.slice(1)}}</p>
    </div> -->
    <NuxtLink to="/projects/portfolio" class="project w-full rounded-3xl relative">
      <video
        ref="video1"
        @mouseleave="pauseVideo(video1)"
        @mouseover="playVideo(video1)"
        class="project__video"
        muted
        loop
        playsinline
        preload="metadata"
        src="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-portafolio.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLXBvcnRhZm9saW8ubXA0IiwiaWF0IjoxNjgzMDQ2MTAxLCJleHAiOjE3MTQ1ODIxMDF9.uQ1y74JFXzavfBujeI86fnTm288JE6hgybCKnQB52AI&t=2023-05-02T16%3A48%3A17.876Z"
        poster="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-portafolio.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tcG9ydGFmb2xpby5wbmciLCJpYXQiOjE2ODMwNDY5MDIsImV4cCI6MTcxNDU4MjkwMn0.DW30duqJIim4kTa9ovI9sVKt923uT2g0_4ygC_L3ilU&t=2023-05-02T17%3A01%3A38.763Z"
      ></video>
      <p class="project__title">Portafolio</p>
    </NuxtLink>
    <NuxtLink to="/projects/talk2learn" class="project w-full rounded-3xl relative">
      <video
        ref="video2"
        @mouseleave="pauseVideo(video2)"
        @mouseover="playVideo(video2)"
        class="project__video"
        muted
        loop
        playsinline
        preload="metadata"
        src="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-talk2learn.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLXRhbGsybGVhcm4ubXA0IiwiaWF0IjoxNjgzMDQ2MzYzLCJleHAiOjE3MTQ1ODIzNjN9.pa38qyK_ezSFpOAnxKiUm2yZ2R6AIUSKsMndZkGHjlc&t=2023-05-02T16%3A52%3A40.077Z"
        poster="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-talk2learn.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tdGFsazJsZWFybi5wbmciLCJpYXQiOjE2ODMwNDY5MjUsImV4cCI6MTcxNDU4MjkyNX0.p6bgKl7Zg_FpKCCJzJo1tneNrRk1zcxEp4dJDnHnT88&t=2023-05-02T17%3A02%3A02.708Z"
      ></video>
      <p class="project__title">Talk2learn</p>
    </NuxtLink>
    <NuxtLink to="/projects/datain" class="project w-full rounded-3xl relative">
      <video
        ref="video3"
        @mouseleave="pauseVideo(video3)"
        @mouseover="playVideo(video3)"
        class="project__video"
        muted
        loop
        playsinline
        preload="metadata"
        src="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-datain.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLWRhdGFpbi5tcDQiLCJpYXQiOjE2ODMwNDY1NzcsImV4cCI6MTcxNDU4MjU3N30.HtaYkGRk3c8R6BtWGkeQPr_JwBZO7RMPts9NmGitSqY&t=2023-05-02T16%3A56%3A14.656Z"
        poster="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-datain.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tZGF0YWluLnBuZyIsImlhdCI6MTY4MzA0Njk0MCwiZXhwIjoxNzE0NTgyOTQwfQ.bqtRvDW3x1Vuz0_N8uxOey9PilO3gANKZCv0Wwtho3k&t=2023-05-02T17%3A02%3A17.120Z"
      ></video>
      <p class="project__title">Datain</p>
    </NuxtLink>
    <NuxtLink to="/projects/frutosdelcampo" class="project w-full rounded-3xl relative">
      <video
        ref="video4"
        @mouseleave="pauseVideo(video4)"
        @mouseover="playVideo(video4)"
        class="project__video"
        muted
        loop
        playsinline
        preload="metadata"
        src="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-frutosdelcampo.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLWZydXRvc2RlbGNhbXBvLm1wNCIsImlhdCI6MTY4MzA0NjU4NiwiZXhwIjoxNzE0NTgyNTg2fQ.2RlFJzg_Y4UBw3B_0xVK7ofz22C8rAaeX_Y88MxWvtk&t=2023-05-02T16%3A56%3A23.719Z"
        poster="https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-frutosdelcampo.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tZnJ1dG9zZGVsY2FtcG8ucG5nIiwiaWF0IjoxNjgzMDQ2OTUxLCJleHAiOjE3MTQ1ODI5NTF9.JbdxZ12M80WCUPgr72sp21I8y_MVNBMmEk3BRdjP1NI&t=2023-05-02T17%3A02%3A28.764Z"
      ></video>
      <p class="project__title">Frutos del Campo</p>
    </NuxtLink>
  </div>
</template>

<script setup>
const video1 = ref();
const video2 = ref();
const video3 = ref();
const video4 = ref();

const projects = ref([
  {
    name: "portafolio",
    url: "https://porfolio-juanesmanrique.vercel.app",
    video_portafolio: null,
  },
  /*  {
    name:'talk2learn',
    url: 'https://porfolio-juanesmanrique.vercel.app'
  }, */
]);

function playVideo(v) {
  v.play();
  /* console.log(v); */
}

function pauseVideo(v) {
  v.pause();
}
</script>

<style>
.main__container {
  width: calc(100% - 2em);
  grid-template-columns: repeat(auto-fit, minmax(30em, 1fr));
  grid-gap: 2em;
  gap: 2em;
}

@media (max-width: 540px) {
  .main__container {
    grid-template-columns: repeat(auto-fit, minmax(15em, 1fr));
  }
}

.project {
  transition: all 0.3s linear;
  color: #e0e0e0;
  background: var(--negro);
  box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b,
    inset 0 0 0 #353535;
  overflow: hidden;
  animation: aparecer 0.8s ease 1 both;
}

.project__video {
  width: 100%;
  height: 100%;
  position: relative;
  z-index: 1;
  opacity: 0.1;
  transform: scale(1.4);
  transition: all 0.5s ease;
  cursor: pointer;
}

.project__video:hover {
  transform: scale(1.1);
  opacity: 0.8;
}

.project__title {
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
  .project__title {
    font-size: 30px;
  }
}
</style>
