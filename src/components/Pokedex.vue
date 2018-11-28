<template>
  <ul>
    <Pokemon 
      v-for="pokemon in pokedex"
      v-bind:key="pokemon.pokemon"
      v-bind:pokemon="pokemon"
    />
  </ul>
</template>

<script>
import Pokemon from './Pokemon';

export default {
  props: {
    pokedex: Array
  },
  components: {
    Pokemon
  }
};
</script>

<style>
ul {
  list-style: none;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  grid-gap: 50px;
}
</style>
