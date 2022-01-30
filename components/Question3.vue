<template>
  <body class="antialiased text-white">
    <div class="flex w-full h-screen justify-evenly items-center">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-5xl text-center">
          Fase 3
        </h1>
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono text-justify">
            {{ questions[2]['question']}}
           
          </p>
          <label 
            :for="key" 
            class="block mt-4 border border-white rounded-lg py-2 px-6 text-lg"
            :key="index"
            v-for="(answer,key, index) in questions[2]['answers']"
            :class="{'cursor-pointer' : selected == ''}"

          >
            <input 
              type="radio" 
              :id="key" 
              class="hidden" 
              :value="key"
              :disabled="selected != ''"
              @click=checkAnswer($event) 
              @change=onChange($event)
            >
              {{ answer }}
          </label>
        </div>
      </div>
      <div class="items-center grid justify-items-center">
        <p class="text-2xl mb-1">
          Survive Game
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
      selected: '',
      questions: [
        {
          question:
            " Você acordou na floresta, tonto e com uma grande dor de cabeça, sem nenhuma memória de como foi parar ali. Um barulho cada vez mais intenso foi o que despertou você desse apagão. Após abrir os olhos e levantar-se, você observa uma manada de búfalos vindo em sua direção, a pouquíssimos metros de distância. O que você faz?",
          answers: {
            a: "Corre o mais rápido possível",
            b: "Sobe na árvore",
            c: "Se finge de morto"},
            correctAnswer: "b"
        },
        {
          question:
            " Ao ver que a manada passou, você desce da árvore e começa a explorar a região em busca de respostas. Não muito distante dali, você encontra um acampamento abandonado e um bilhete com instruções, deixado para trás. Antes que você possa alcançar o bilhete, um homem aparece com uma marreta gritando e avançando em sua direção. No seu corpo a adrenalina dispara. O que você faz?",
          answers: {
            a: "Foge para bem longe",
            b: "Pega o bilhete e foge para bem longe",
            c: "Puxa toda a coragem do coração e enfrente o homem"},
            correctAnswer: "c"
        },
        {
          question:
            " Você finalmente consegue ler o bilhete: “Vamos fazer parecer um acidente. Misture o conteúdo deste frasco na comida dele. O remédio vai começar a fazer efeito depois de 30 minutos. Quando ele estiver completamente apagado, leve-o até o pé da árvore mais alta no início da floresta e direcione a manada de búfalos em sua direção. Estaremos esperando no laboratório ao norte do acampamento.” O que você faz?",
          answers: {
            a: "Foge e liga para a polícia",
            b: "Amarra o homem e vai ao laboratório",
            c: "Mata o homem, pega a marreta e vai ao laboratório"},
            correctAnswer: "a"
        },
      ]
    }
    
  },
  methods: {
    onChange:function(event){
       this.selected = event.target.value
       console.log(this.selected)
       if(this.selected == 'a')
       {
         this.$router.push('/play/3/outcome/1')
       }
       else if(this.selected == 'b')
       {
         this.$router.push('/play/3/outcome/2')
       }
       else{
         this.$router.push('/play/3/outcome/3')
       }
    },
    checkAnswer(e){
      console.log(this.selected)
    }
  }
}
</script>

<style scoped>
label:hover {
  background: var(--base-color);
}


</style>