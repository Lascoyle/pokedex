<template>
  <div id="pokedex-btn-options">
    <button class="pokedex-btn-option select"></button>
    <button class="pokedex-btn-option start"></button>
  </div>
</template>

<script>
export default {
    name: 'PokedexBtnOptions'
}
</script>

<style>
#pokedex-btn-options {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 30%;
  margin-left: 15px;
  align-self: flex-end;

}

.pokedex-btn-option {
  width: 45px;
  height: 15px;
  border-radius: 50px;
  background: rgb(59, 58, 68);
  transform: rotate(-25deg);
  border-color: gray;
}
</style>