<template>
  <div class="px-5 pt-10 xl:px-0 ">
    <template v-for="(project, index) in projects" :key="index">
      <div v-if="project.route == router.params.project" class="seccion intro w-full relative">
        <video
          class="seccion__video w-full object-cover"
          muted
          autoplay
          loop
          playsinline
          preload="auto"
          loading="lazy"
          :src="project.video"
        ></video>
        <article class="seccion__article h-max grid grid-cols-3 absolute">
          <div class="seccion__col w-full">
            <span class="seccion__span">Proyecto</span>
              <h2 class="seccion__h2">{{project.name}}</h2>
              <span class="seccion__span">Cliente</span>
              <h2 class="seccion__h2">{{project.client}}</h2>
          </div>
          <div class="seccion__col w-full flex items-center">
            <p class="seccion__p text-lg">{{project.description}}</p>
          </div>
          <div class="seccion__col px-5 w-full flex items-center text-center">
            <a target="_blank" rel="noopener noreferrer" class="seccion__a w-full" :href="project.url">Ver proyecto</a>
            </div>
        </article>
      </div>
    </template>
  </div>
</template>

<script setup>
const router = useRoute();

const projects = ref([
  {
    name: "Portafolio",
    client: "Personal",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi laborum illo saepe atque nulla magnam, hic ut ullam quibusdam itaque iste nihil laboriosam maxime labore impedit, quam est commodi aliquam.",
    video: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-portafolio.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLXBvcnRhZm9saW8ubXA0IiwiaWF0IjoxNjgzMDQ2MTAxLCJleHAiOjE3MTQ1ODIxMDF9.uQ1y74JFXzavfBujeI86fnTm288JE6hgybCKnQB52AI&t=2023-05-02T16%3A48%3A17.876Z",
    image: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-portafolio.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tcG9ydGFmb2xpby5wbmciLCJpYXQiOjE2ODMwNDY5MDIsImV4cCI6MTcxNDU4MjkwMn0.DW30duqJIim4kTa9ovI9sVKt923uT2g0_4ygC_L3ilU&t=2023-05-02T17%3A01%3A38.763Z",
    route: "portfolio",
    url: "https://porfolio-juanesmanrique.vercel.app/"
  },
  {
    name: "Landing page",
    client: "Talk2learn",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi laborum illo saepe atque nulla magnam, hic ut ullam quibusdam itaque iste nihil laboriosam maxime labore impedit, quam est commodi aliquam.",
    video: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-talk2learn.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLXRhbGsybGVhcm4ubXA0IiwiaWF0IjoxNjgzMDQ2MzYzLCJleHAiOjE3MTQ1ODIzNjN9.pa38qyK_ezSFpOAnxKiUm2yZ2R6AIUSKsMndZkGHjlc&t=2023-05-02T16%3A52%3A40.077Z",
    image: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-talk2learn.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tdGFsazJsZWFybi5wbmciLCJpYXQiOjE2ODMwNDY5MjUsImV4cCI6MTcxNDU4MjkyNX0.p6bgKl7Zg_FpKCCJzJo1tneNrRk1zcxEp4dJDnHnT88&t=2023-05-02T17%3A02%3A02.708Z",
    route: "talk2learn",
    url: "https://www.talk2learn.co/"
  },
  {
    name: "Landin page",
    client: "Datain",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi laborum illo saepe atque nulla magnam, hic ut ullam quibusdam itaque iste nihil laboriosam maxime labore impedit, quam est commodi aliquam.",
    video: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-datain.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLWRhdGFpbi5tcDQiLCJpYXQiOjE2ODMwNDY1NzcsImV4cCI6MTcxNDU4MjU3N30.HtaYkGRk3c8R6BtWGkeQPr_JwBZO7RMPts9NmGitSqY&t=2023-05-02T16%3A56%3A14.656Z",
    image: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-datain.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tZGF0YWluLnBuZyIsImlhdCI6MTY4MzA0Njk0MCwiZXhwIjoxNzE0NTgyOTQwfQ.bqtRvDW3x1Vuz0_N8uxOey9PilO3gANKZCv0Wwtho3k&t=2023-05-02T17%3A02%3A17.120Z",
    route: "datain",
    url: "https://www.datain.co/"
  },
  {
    name: "Landin page",
    client: "Frutos del Campo CTA",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi laborum illo saepe atque nulla magnam, hic ut ullam quibusdam itaque iste nihil laboriosam maxime labore impedit, quam est commodi aliquam.",
    video: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/videos/video-frutosdelcampo.mp4?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvdmlkZW9zL3ZpZGVvLWZydXRvc2RlbGNhbXBvLm1wNCIsImlhdCI6MTY4MzA0NjU4NiwiZXhwIjoxNzE0NTgyNTg2fQ.2RlFJzg_Y4UBw3B_0xVK7ofz22C8rAaeX_Y88MxWvtk&t=2023-05-02T16%3A56%3A23.719Z",
    image: "https://isafdkvqpndwdizemlcw.supabase.co/storage/v1/object/sign/resources/projects/images/foto-frutosdelcampo.png?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1cmwiOiJyZXNvdXJjZXMvcHJvamVjdHMvaW1hZ2VzL2ZvdG8tZnJ1dG9zZGVsY2FtcG8ucG5nIiwiaWF0IjoxNjgzMDQ2OTUxLCJleHAiOjE3MTQ1ODI5NTF9.JbdxZ12M80WCUPgr72sp21I8y_MVNBMmEk3BRdjP1NI&t=2023-05-02T17%3A02%3A28.764Z",
    route: "frutosdelcampo",
    url: "https://frutosdelcampocta.com/"
  },
])
</script>

<style scoped>
  .seccion {
    animation: aparecer 1s ease 1 both;
  }

  .seccion.intro {
    color: #e0e0e0;
    border-radius: 2em;
    background: #282828;
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;
    transition: all .3s linear;
    overflow: hidden;
  }

  .seccion__video {
    height: 70vh;
    border-radius: 2em;
    pointer-events: none;
  }

  .seccion__article {
    width: calc(100% - 4em);
    padding: 2em;
    bottom: 2em;
    left: 2em;
    background-color: #282828;
    background-color: var(--negro);
    border-radius: 2em;
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;
    animation: aparecer 1s ease .2s 1 both;
  }

  .seccion__col {
    font-size: 1.2em;
  }
  .seccion__span {
    display: block;
    margin: 0 0 0.2em;
    color: grey;
  }

  .seccion__h2 {
    margin: 0 0 0.5em;
    font-size: 1.5em;
    font-weight: 900;
  }

  .seccion__p {
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;
  }

  .seccion__a {
    padding: 1em 0;
    box-shadow: 0.1em 0.1em 0.5em #1b1b1b, -0.1em -0.1em 0.5em #353535, inset 0 0 0 #1b1b1b, inset 0 0 0 #353535;
    transition: all .3s linear;
    color: #e0e0e0;
    border-radius: 2em;
    background: var(--negro);
  }

  .seccion__a:hover {
    transform: scale(1.1);
  }

  @keyframes aparecer {
    0% {
      transform: translateY(15em);
      opacity: 0;
    }

    100% {
      transform: translateY(0);
      opacity: 1;
    }
  }
</style>
