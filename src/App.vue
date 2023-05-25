<script setup>
import Item from './components/Item.vue'
</script>

<script>
import Dados from './Dados/Services.json'
export default {
  data() {
    return{
      servicos: null
    }
  },
  mounted() {
    this.servicos = Dados;
    console.log(Dados);
  }
}
</script>

<template>    
    <img src="./assets/tesoura.png" class="logo" alt="Barbearia"/> 
    <h1 style="font-size: large;">Seja bem vindo(a)!</h1>
  <hr /> 
  <div class="items">
    <Item
    v-for="servico, index in servicos"
    :key="index"
    :item="servico"
    />
  </div>
</template>

<style scoped>
html{
  background: url("./assets/barbearia.jpg");
  background-repeat: no-repeat;
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.items{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
