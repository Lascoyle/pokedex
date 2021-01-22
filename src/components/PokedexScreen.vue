<template>
  <div id="pokedex-screen">
      <div id="pokedex-screen-frame">
          <div id="pokedex-screen-image">
              
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'PokedexScreen'
}
</script>

<style>
#pokedex-screen {
    width: 90vw;
    height: 50vh;
}

#pokedex-screen-frame {
    background-color:rgb(59, 58, 68);
    border-radius: 15px;
    border-bottom-right-radius: 40px;
    padding: 5%;
    width: inherit;
    height: inherit;
}

#pokedex-screen-image {
    background-color:rgb(148, 197, 84);
    border-radius: 5px;
    width: 80%;
    height: 80%;
    margin: auto;
    margin-top: 10px;
}
</style>