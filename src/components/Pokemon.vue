<template>
  <li>
    <img v-bind:src="pokemon.url_image" alt="" />
    <h2>{{ pokemon.pokemon }}</h2>
    <p>Type: {{ pokemon.type_1 }}</p>
    <p>Attack: {{ pokemon.attack }}</p>
    <p>Defense: {{ pokemon.defense }}</p>
  </li>
</template>

<script>
export default {
  props: {
    pokemon: Object
  }
};
</script>

<style>

</style>
