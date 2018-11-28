<template>
  <li v-bind:style="{ background: pokemon.color_1 }">
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
li {
  line-height: 4%;
  padding: 2%;
  object-fit: contain;
  width: 200px;
}
img {
  max-width: 100%;
}

</style>
