<script setup>
const pokemon = defineProps(["name", "xp", "height", "img", "loading"]);
</script>
<template>
  <div
    class="card cardPokemonSelected"
    :class="loading ? '' : 'animate__animated animate__flipInY'"
  >
    <img
      :src="pokemon.img"
      height="250"
      class="card-img-top pt-2"
      :alt="pokemon.name"
    />
    <div class="card-body">
      <h5 class="card-title text-center">{{ pokemon.name }}</h5>
      <hr />
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


<style scoped >
.cardPokemonSelected {
  height: 450px;
  background: rgb(72, 63, 251);
  background: radial-gradient(
    circle,
    rgba(250, 242, 0, 0.6) 0%,
    rgba(245, 32, 4, 0.883) 100%
  );
}
</style>