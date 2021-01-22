<template>
  <div id="pokedex-search">
      <form id="pokedex-searchbar" action="GET">
          <input id="pokedex-searchbar-input" type="text" placeholder="Search a Pokemon...">
      </form>
  </div>
</template>

<script>
export default {
    name: 'PokedexSearch'
}
</script>

<style>

#pokedex-searchbar-input {
    padding: 5%;
    margin-top: 3%;
    width: 80vw;
    height: 5vh;
    border-radius: 100px;
    border: none;
    background:  rgb(233, 129, 129);
    color: white;
    font-weight: bold;
}
</style>