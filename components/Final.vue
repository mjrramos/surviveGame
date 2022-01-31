<template>
  <div class="antialiased text-white">
    <div class="start min-h-screen w-screen flex justify-center items-center flex-col-reverse lg:flex-row lg:justify-around">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-5xl text-center">
          Foge e liga para a polícia
        </h1>
        <NavBreadcrumb idf="3" />
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono mb-6">
            Você informa a polícia o que aconteceu e passa a localização do laboratório. Chegando lá ela se depara com um sítio de produção de cocaína e prende todos os presentes. As evidências sugerem que você ainda pode estar em perigo, por este motivo a polícia lhe coloca no programa de proteção à testemunha e você sobrevive para vivenciar uma nova história. Parabéns, você ganhou!
          </p>
          <div class="items-center grid justify-items-center">
            <img class="lg:max-w-xl h-max w-max rounded-2xl" src="~/assets/images/start.gif" alt="">
          </div>
          <div class="flex justify-end">
            <a class="mt-4 span inline-block bg-base p-5 rounded-full text-base text-white tracking-wide" href="/">Voltar ao início</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  label:hover {
    background: var(--base-color);
  }
</style>