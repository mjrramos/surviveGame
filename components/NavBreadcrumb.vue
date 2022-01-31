<template>
  
  <header>
    <nav class="mt-4">
      <ul class="navigation flex justify-center">
        <li v-show=" idf != ''" class=""><a href="/play/1/outcome/2" class="">Fase 1</a></li>
        
        <li v-show=" idf != '1'" class=""><a href="/play/2/outcome/3" class="">Fase 2</a></li>

        <li v-show=" idf == '3'" class=""><a href="/" class="">Início</a></li>
      </ul>
    </nav>
  </header>

</template>

<script>
  
  export default {
    props: [
    'idf'
    ],
    data(){
      return{
        id: this.idf
      }
    }
    
  }

</script>

<style scoped>

ul {
  list-style: none;
}
.navigation {
  list-style: none;
}

.navigation li {
  display: inline-block;
  padding: 0 1rem;
  text-transform: uppercase;
}

/* .navigation li a {
  transition: 0.3s;
  color: #ffff;
} */






</style>