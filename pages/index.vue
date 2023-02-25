<template>
  <Circles />
  <div class="w-full h-screen flex justify-center fixed z-10 overflow-auto" style="background: var(--negro-7);">
    <div class="max-w-5xl w-full grid" style="grid-template-rows: auto 1fr auto;">
      <LayoutNavbar />
      <div class="">
        <div class="w-full flex flex-col justify-center items-center font-semibold " style="height: 80vh;">
          <p class=" text-7xl opacity-90">Juan Sanchez</p>
          <p class=" text-7xl opacity-90">Frontend Developer</p>
        </div>
      </div>
      <LayoutFooter />
    </div>
  </div>
</template>

<style>
  * {
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
  vertical-align: baseline;
}

body {
  font-family: Montserrat,sans-serif;
  min-height: 100vh;
  background-color: var(--negro);
  color: var(--blanco);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

:root {
  --blanco: #e0e0e0;
  --blanco-2: rgba(255,255,255,.2);
  --negro: #181818;
  --negro-5: rgba(0, 0, 0, 0.5);
  --negro-7: rgba(0, 0, 0, 0.75);
}

@media screen and (prefers-color-scheme:light){
  :root {
    --blanco: #181818;
    --blanco-2: rgba(0,0,0,.2);
    --negro: #e0e0e0;
    --negro-5: rgba(255, 255, 255, 0.5);
    --negro-7: rgba(255, 255, 255, 0.75);
  }
}
</style>