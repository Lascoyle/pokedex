<template>
  <div id="pokedex-btn-options">
    <div id="pokedex-btn-options-group">
      <button class="pokedex-btn-option select"></button>
      <button class="pokedex-btn-option start"></button>
    </div>
    <div id="pokedex-btn-options-labels">
      <p class="pokedex-btn-options-label">Select</p>
      <p class="pokedex-btn-options-label">Start</p>
    </div>
  </div>
</template>

<script>
export default {
    name: 'PokedexBtnOptions'
}
</script>

<style>
#pokedex-btn-options {
  width: 30%;
  margin-left: 15px;
  margin-bottom: -20px;
  align-self: flex-end;
}

#pokedex-btn-options-group, #pokedex-btn-options-labels {
  display: flex;
  justify-content: space-between;
}

#pokedex-btn-options-group {
  margin-top: 10px;
  margin-bottom: 2px ;
}

.pokedex-btn-options-label {
  transform: rotate(-25deg);
  color: rgb(59, 58, 68);
  text-transform: uppercase;
  font-size: 1.1rem;
  margin-left: 10px;
  font-weight: 600;
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