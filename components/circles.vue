<template >
  <div class="circles__container w-full h-full top-0 left-0 fixed">
    <svg class="circle1 w-6/12 h-3/6 absolute top-0 left-0" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
      <path class="path" d="M46.2,-11.4C52.1,3.1,43.7,25.8,27.5,37.5C11.4,49.1,-12.6,49.7,-32.6,36.9C-52.7,24.2,-69,-1.7,-62.9,-16.5C-56.9,-31.3,-28.4,-34.8,-4.1,-33.5C20.2,-32.1,40.3,-25.9,46.2,-11.4Z" transform="translate(100 100)" />
    </svg>
    <svg class="circle2 w-6/12 h-3/6 absolute top-0 right-0" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
      <path class="path" d="M38.2,-51.3C46.1,-38.9,46.7,-23.6,50.9,-7.8C55.1,8,62.8,24.4,59.4,38.1C56,51.7,41.4,62.7,25.2,68.1C9,73.6,-8.9,73.4,-23.5,67C-38.1,60.6,-49.4,47.8,-51.7,34.4C-53.9,21,-47.1,7,-44.6,-8C-42.1,-23,-44,-38.9,-37.3,-51.5C-30.6,-64,-15.3,-73.3,-0.1,-73.2C15.2,-73.1,30.3,-63.7,38.2,-51.3Z" transform="translate(100 100)" />
    </svg>
    <svg class="circle3 w-6/12 h-3/6 absolute bottom-0 left-0" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
      <path class="path" d="M48.9,-67.7C64,-66.4,77.5,-53.9,75.6,-39.8C73.8,-25.8,56.8,-10,48.3,2.6C39.8,15.3,39.7,24.8,35.5,32C31.3,39.3,22.8,44.1,14.3,44.7C5.9,45.3,-2.6,41.7,-15.1,42.2C-27.6,42.8,-44.1,47.6,-52.1,42.7C-60.1,37.8,-59.7,23.2,-55.4,11.8C-51.1,0.4,-42.8,-7.7,-36.9,-15.3C-31,-23,-27.5,-30.2,-21.8,-35.9C-16,-41.5,-8,-45.5,4.4,-52.4C16.9,-59.3,33.8,-69.1,48.9,-67.7Z" transform="translate(100 100)" />
    </svg>
    <svg class="circle4 w-6/12 h-3/6 absolute bottom-0 right-0" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
      <path class="path" d="M47.7,21.4C38.6,43.3,-8,37.4,-22.2,12.6C-36.4,-12.3,-18.2,-56,5.1,-53.1C28.4,-50.1,56.8,-0.5,47.7,21.4Z" transform="translate(100 100)" />
    </svg>
  </div>
</template>

<style>
  .circles__container {
    z-index: 1;
    filter: blur(40px);
    animation:circle1 50s linear infinite both;
  }

  .circles__container svg {
    animation:circle1 50s linear infinite both;
  }

  @keyframes circle1{
    from{
      transform:rotate(0deg) scale(2);
    }
    to{
      transform:rotate(360deg) scale(2);
    }
  }

  .circles__container .circle1 .path {
    fill: #2e8b57;
  }

  .circles__container .circle2 .path {
    fill: rgb(111, 0, 155);
  }

  .circles__container .circle3 .path {
    fill: rgb(165, 127, 1);
  }

  .circles__container .circle4 .path {
    fill: rgb(0, 59, 155);
  }

  /* @keyframes aparecer1{
    from{
      opacity: 0;
      transform: translateY(50%);
    }
    to{
      opacity: 1;
      transform: translateY(0%);
    }
  } */
</style>