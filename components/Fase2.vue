<template>
  <body class="antialiased text-white">
    <div class="flex w-full h-screen justify-center items-center">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-5xl text-center">
          Puxa toda coragem do coração e enfrenta o homem!
        </h1>
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono mb-6">
            Você consegue desviar da primeira marretada do homem, que fica ocioso por um curto período, o suficiente para você acertá-lo em cheio na cabeça e apagá-lo no chão.
          </p>
          <div class="items-center grid justify-items-center">
            <img class="lg:max-w-xl rounded-full" src="~/assets/images/run.gif" alt="">
          </div>
          <div class="flex justify-end">
            <a class="span inline-block bg-base p-5 rounded-full text-base text-white tracking-wide" href="/play/3">Próxima fase</a>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<style scoped>
  label:hover {
    background: var(--base-color);
  }
</style>