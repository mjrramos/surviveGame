<template>
  <div class="antialiased text-white">
    <div class="start min-h-screen w-screen flex justify-center items-center flex-col-reverse lg:flex-row lg:justify-around">
      <div class="w-full max-w-4xl">
        <h1 class="font-bold text-4xl text-center">
          Fase 1
        </h1>
        
        <div class="bg-base-second p-12 rounded-lg shadow-sm w-full mt-10">
          <p class="text-xl font-mono text-justify">
            {{ questions[i]['question']}}
           
          </p>
          <label 
            :for="key" 
            class="block mt-4 border border-white rounded-lg py-2 px-6 text-lg"
            :key="index"
            v-for="(answer,key, index) in questions[i]['answers']"
            :class="{'cursor-pointer' : selected == ''}"

            
          >
            <input 
              type="radio" 
              :id="key" 
              class="hidden" 
              :value="key"
              :disabled="selected != ''"
              @click=onChange($event)
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
  </div>
</template>

<script>

export default {
  data(){
    return {
      i:0,
      selected: '',
      questions: [
        {
          id:1,
          question:
            " Você acordou na floresta, tonto e com uma grande dor de cabeça, sem nenhuma memória de como foi parar ali. Um barulho cada vez mais intenso foi o que despertou você desse apagão. Após abrir os olhos e levantar-se, você observa uma manada de búfalos vindo em sua direção, a pouquíssimos metros de distância. O que você faz?",
          answers: {
            a: "Corre o mais rápido possível",
            b: "Sobe na árvore",
            c: "Se finge de morto"},
            correctAnswer: "b"
        },
        {
          id:2,
          question:
            " Ao ver que a manada passou, você desce da árvore e começa a explorar a região em busca de respostas. Não muito distante dali, você encontra um acampamento abandonado e um bilhete com instruções, deixado para trás. Antes que você possa alcançar o bilhete, um homem aparece com uma marreta gritando e avançando em sua direção. No seu corpo a adrenalina dispara. O que você faz?",
          answers: {
            a: "Foge para bem longe",
            b: "Pega o bilhete e foge para bem longe",
            c: "Puxa toda a coragem do coração e enfrente o homem"},
            correctAnswer: "c"
        },
        {
          id:3,
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
    onChange(event){
       this.selected = event.target.value
       if(this.selected == 'a')
       {
         this.selected == ''
         this.$router.push('/play/1/outcome/1')
       }
       else if(this.selected == 'b')
       {
         this.selected == ''
         this.$router.push('/play/1/outcome/2')
       }
       else{
         this.selected == ''
         this.$router.push('/play/1/outcome/3')
       }
    },
    checkAnswer(){


    }
  }
}
</script>

<style scoped>
label:hover {
  background: var(--base-color);
}


</style>