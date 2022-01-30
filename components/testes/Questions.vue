<template>
  <body class="antialiased text-white">
    <div class="flex w-full h-screen justify-center items-center">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-5xl text-center">
          Sobe na árvore!
        </h1>
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono mb-6">
            Você sobe na árvore e escapa por pouco da manada.
          </p>
          <div class="items-center grid justify-items-center">
            <img class="lg:max-w-xl rounded-full" src="https://www.dropbox.com/s/0x7d1kgrkc186iv/GIF2.gif?raw=1" alt="">
          </div>
          <div class="flex justify-end">
            <a class="span inline-block bg-base p-5 rounded-full text-base text-white tracking-wide" href="/play/2">Próxima fase</a>
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