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
}
</style>
