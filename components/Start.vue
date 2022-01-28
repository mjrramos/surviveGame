<template>
  <div class="container">
    <div class="flex w-full h-screen justify-center backcolor">
      <div class="font-bold text-9xl text-center items-center text-gray-700">
        <h1>Survive Game</h1>
        <p class="text-5xl">As suas escolhas definem o seu caminho!</p>
        <img src="~/assets/images/start.gif" alt="" />
        <button>
          <a href="">Start</a>
        </button>
      </div>
      <!-- <div class="flex justify-center">
        <img src="~/assets/images/start.gif" alt="" />
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  setup() {},
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Amatic+SC&display=swap");
.backcolor {
  background: rgba(24, 44, 59, 1);
  font-family: "Amatic SC", sans-serif;
}

.backcolor h1,
p {
  color: #fff;
}
</style>