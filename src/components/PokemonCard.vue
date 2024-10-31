<template>
  <div class="card cardPokemon" :class="loading ?'':'animate__animated animate__flipInY'">
    <img 
    v-if="pokemon.name" :src="pokemon.img" class="card-img-top pt-2" :alt="pokemon.name" >
    <img v-else src="../assets/egg_pokemon.svg" class="card-img-top pt-2" alt="???">
    <div class="card-body">
      <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
      <hr>
      <div class="row">
        <section class="col">
          <strong>XP:</strong>
          <span>{{ pokemon.xp }}</span>
        </section>
        <section class="col">
          <strong>Altura:</strong>
          <span>{{ pokemon.height }}</span>
        </section>
        
      </div>
    </div>
  </div>
</template>

<script setup>
const pokemon = defineProps(['name', 'xp', 'height', 'img', 'loading'])
</script>

<style scoped>
.cardPokemon {
  height: 75vh;
  background: rgb(49,50,51);
  background: radial-gradient(circle, rgba(49,50,51,3) 28%, rgba(35,35,38,0) 63%, rgba(26,25,29,0.9139240506329114) 100%);
  cursor: pointer;
}

.cardPokemon img{
  height: 250px;
}

.cardPokemon:hover{
  background: rgb(179,179,186);
  background: radial-gradient(circle, rgba(179,179,186,0.2) 39%, rgba(53,55,57,0) 83%);
}

.cardPokemon img:hover{
  padding: .1rem;
}

@media (max-width: 768px) {
  .CardPokemonSelected{
    height: 30vh;
    width: 40%;
    margin: 0 auto 10px auto;
  }
  .CardPokemonSelected img{
    height: 100px;
  }
}
</style>