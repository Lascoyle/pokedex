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
    justify-content: flex-end;
    width: 35%;
}

.pokedex-btn-action {
    display: block;
    width: 40px;
    height: 40px;
    border: none;
    border-radius: 100px;
    background-color:rgb(59, 58, 68);
    margin-left: 10px;
}

.cancel {
    margin-top: 15px
}


</style>