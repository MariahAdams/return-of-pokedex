<template>
  <div id="app">
    <h1>Gotta Catch 'Em All...Again</h1>
    <Header 
      v-bind:filter="filter"
      v-bind:types="pokeTypes"
    />
    <Pokedex v-bind:pokedex="filteredPokemon"/>
  </div>
</template>

<script>
import Pokedex from './components/Pokedex';
import Header from './components/Header';
import pokedexApi from './services/pokedexApi';

export default {
  name: 'app',
  data() {
    return {
      pokedex: pokedexApi.getAll(),
      filter: {
        type: ''
      }
    };
  },
  components: {
    Pokedex,
    Header
  },
  computed: {
    pokeTypes() {
      const types = [];
      this.pokedex.forEach(pokemon => {
        if(!types.includes(pokemon.type_1)) {
          types.push(pokemon.type_1);
        }
      });
      return types;
    },
    filteredPokemon() {
      return this.pokedex.filter(pokemon => {
        const hasType = !this.filter.type || pokemon.type_1 === this.filter.type;
        return hasType;
      });
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
