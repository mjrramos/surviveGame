<template>

  <div>
    <div class="start min-h-screen w-screen flex justify-center items-center flex-col-reverse lg:flex-row lg:justify-around">
      <div class="mt-5 text-center">
        <h1 class="text-6xl mb-3 text-bold">
          Survive <span class="text-red-600">Game</span> 
          <br/>
        </h1>
        <p class="text-base mb-5">Seu destino depende das suas escolhas!</p> 
        
        
          <a class="span inline-block bg-base-second px-12 py-2 rounded-full text-3xl text-white tracking-wide" href="/play/1">Iniciar</a>
        
      </div>
      <img class="w-screen lg:max-w-xl rounded-3xl" src="~/assets/images/start.gif" alt="">
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    
  },
}
</script>

<style scoped>
  p, .span {
    font: 400 1rem var(--text-font);
    -webkit-font-smoothing: antialiased;
  }
</style>