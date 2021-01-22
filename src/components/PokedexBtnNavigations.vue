<template>
  <div id="pokedex-btn-navigations">
      <button class="pokedex-btn-navigation up"></button>
      <div class="btns-group">
        <button class="pokedex-btn-navigation left"></button>
        <div class="pokedex-btn-navigation center">
          <div class="center-rounded"></div>
        </div>
        <button class="pokedex-btn-navigation right"></button>
      </div>
      <button class="pokedex-btn-navigation down"></button>
  </div>
</template>

<script>
export default {
    name: 'PokedexBtnNavigations'
}
</script>

<style>
#pokedex-btn-navigations {
  width: 30%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.pokedex-btn-navigation {
  display: block;
  width: 30px;
  height: 30px;
  border: none;
  background-color:rgb(59, 58, 68);
}

.btns-group {
  display: flex;
}

.up {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}

.down {
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
}

.left {
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
}

.right {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}

.center-rounded {
  background-color:rgb(100, 98, 114);
  width: 80%;
  height: 80%;
  border-radius: 50px;
  margin: 0 auto;
  margin-top: 10%;
}
</style>