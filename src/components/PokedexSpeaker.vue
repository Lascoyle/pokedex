<template>
  <div id="pokedex-speaker">
      <div class="pokedex-speaker-hole"></div>
      <div class="pokedex-speaker-hole"></div>
      <div class="pokedex-speaker-hole"></div>
      <div class="pokedex-speaker-hole"></div>
      <div class="pokedex-speaker-hole"></div>
      <div class="pokedex-speaker-hole"></div>
  </div>
</template>

<script>
export default {
    name: 'PokedexSpeaker'
}
</script>

<style>
#pokedex-speaker {
    display: flex;
    justify-content: space-between;
    width: 25%;
    height: 70px;
    align-self: flex-end;
    margin: 10px;
    transform: rotate(-25deg);
}

.pokedex-speaker-hole {
    height: inherit;
    width: 10px;
    background:  rgb(189, 57, 57);
    border-radius: 50px;
}
</style>