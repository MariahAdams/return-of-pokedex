<template>
  <div id="app">
    <h1>Gotta Catch 'Em All...Again</h1>
    <Pokedex />
  </div>
</template>

<script>
import Pokedex from './components/Pokedex';

export default {
  name: 'app',
  components: {
    Pokedex
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
