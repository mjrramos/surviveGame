<template>
  <div class="antialiased text-white">
    <div class="flex w-full h-screen justify-center items-center">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-5xl text-center">
          Corre o mais rápido possível e...
        </h1>
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono mb-6">
            A sua corrida não foi suficiente para superar a da manada. Você morreu atropelado.
          </p>
          <div class="items-center grid justify-items-center">
            <img class="lg:max-w-xl rounded-xl" src="~/assets/images/gover.png" alt="">
          </div>
          <div class="mt-4 flex justify-center">
            <a class="button mr-2 inline-block bg-base p-5 rounded-full text-base text-white tracking-wide" href="/play/1">Tente novamente</a>
            <a class="button inline-block bg-base p-5 rounded-full text-base text-white tracking-wide" href="/">Voltar ao início</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  button:hover {
    background: var(--base-color);
  }
</style>