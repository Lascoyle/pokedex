<template>
  <div id="app">
    <pokedex></pokedex>
  </div>
</template>

<script>
import Pokedex from './components/Pokedex.vue'


export default {
  name: 'App',
  components: {
    Pokedex
  }
}
</script>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  font-size: 62.5%;
  background-color: rgb(47, 50, 66);
}

body {
  box-sizing: border-box;
  font-size: 1.6rem;
}

ul {
  list-style-type: none;
}

button:hover {
  cursor: pointer;
}
</style>
