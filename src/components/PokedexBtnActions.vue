<template>
  <div id="pokedex-btn-actions">
      <div class="pokedex-btn-actions-group">
          <button class="pokedex-btn-action cancel"></button>
          <button class="pokedex-btn-action confirm"></button>
      </div>
      <div class="pokedex-btn-actions-labels">
          <p>B</p>
          <p>A</p>
      </div>
  </div>
</template>

<script>
export default {
    name: 'PokedexBtnActions'
}
</script>

<style>
#pokedex-btn-actions {
    width: 33%;
    transform: rotate(-20deg);
}

.pokedex-btn-actions-group, .pokedex-btn-actions-labels {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.pokedex-btn-actions-group {
    background-color: rgb(211, 63, 63);
    padding: 5px;
    border-radius: 50px;
}

.pokedex-btn-actions-labels {
    padding: 5px;
    color: rgb(59, 58, 68);
    font-weight: 600;
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