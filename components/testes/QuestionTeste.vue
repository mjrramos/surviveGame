<template>
  <body class="antialiased text-white">
    <div class="flex w-full h-screen justify-evenly items-center">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-5xl text-center">
          Fase 2
        </h1>
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono text-justify">
            {{ question }}
           
          </p>
          <button 
            class="block mt-4 border border-white rounded-lg py-2 px-6 text-lg"
            :key="index"
            v-for="(answer,index) in answers"
            @click=onChange(answer)
            >
              {{ answer }}
          </button>
        </div>
      </div>
      <div class="items-center grid justify-items-center">
        <p class="text-2xl mb-1">
          Sobreviva!
        </p>
        <img class="lg:max-w-xl rounded-2xl" src="~/assets/images/start.gif" alt="">
      </div>
    </div>
  </body>
</template>

<script>

export default {
  data(){
    return {
      select:false,
      question:
            " Ao ver que a manada passou, você desce da árvore e começa a explorar a região em busca de respostas. Não muito distante dali, você encontra um acampamento abandonado e um bilhete com instruções, deixado para trás. Antes que você possa alcançar o bilhete, um homem aparece com uma marreta gritando e avançando em sua direção. No seu corpo a adrenalina dispara. O que você faz?",
      answers: {
            a: "Foge para bem longe",
            b: "Pega o bilhete e foge para bem longe",
            c: "Puxa toda a coragem do coração e enfrente o homem"},
            correctAnswer: "c"
        }
  },
  methods: {
    onChange:function(event){
       this.selected = event
       const select = event
       console.log('this = ', this.selected)
       console.log('const = ',select)
       if(select == 'Foge para bem longe')
       {
         this.$router.push('/play/2/outcome/1')
       }
       else if(select == 'b')
       {
         this.$router.push('/play/2/outcome/2')
       }
       else{
         this.$router.push('/')
       }
    },
    checkAnswer(){


    }
  }
}
</script>

<style scoped>
button:hover {
  background: var(--base-color);
}


</style>