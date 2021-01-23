<template>
  <div id="pokedex-btn-actions">
      <button class="pokedex-btn-action cancel"></button>
      <button class="pokedex-btn-action confirm"></button>
  </div>
</template>

<script>
export default {
    name: 'PokedexBtnActions'
}
</script>

<style>
#pokedex-btn-actions {
    display: flex;
    justify-content: space-between;
    width: 33%;
    padding: 5px;
    background-color: rgb(211, 63, 63);
    transform: rotate(-20deg);
    border-radius: 50px;
}

.pokedex-btn-action {
    display: block;
    width: 40px;
    height: 40px;
    border-color: gray;
    border-radius: 100px;
    background-color:rgb(59, 58, 68);
}




</style>