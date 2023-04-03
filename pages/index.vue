<template>
  <Circles />
  <div class="w-full h-screen flex justify-center fixed z-10 overflow-auto" style="background: var(--negro-7);">
    <div class="max-w-7xl w-full grid" style="grid-template-rows: auto 1fr auto;">
      <LayoutNavbar />
      <NuxtPage />
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
  background-color: #181818;
  color:#e0e0e0;
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

.texto{
  transition: all .3s linear;
  animation: aparecer 2s ease .6s 1 both;
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