<template>
  <div class="col-4">
    <div class="card p-2 mb-3 cardListPokemon">
      <p class="text-center">{{ pokemon.name }}</p>
      <img 
      :src="urlSvg" class="card-img-top" 
      alt="..."
      height="80"
      />
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const pokemon = defineProps(["name", "urlSvg"]);
</script>

<style scoped>
.cardListPokemon {
  background: rgb(49,50,51);
  background: radial-gradient(circle, rgba(49,50,51,3) 28%, rgba(35,35,38,0) 63%, rgba(26,25,29,0.9139240506329114) 100%);
  cursor: pointer;
}

.cardListPokemon:hover{
  background: rgb(179,179,186);
  background: radial-gradient(circle, rgba(179,179,186,0.2) 39%, rgba(53,55,57,0) 83%);
}

.cardListPokemon img:hover{
  padding: .1rem;
}
</style>