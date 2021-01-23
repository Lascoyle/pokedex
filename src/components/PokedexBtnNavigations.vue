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
  width: 31%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color:  rgb(211, 63, 63);
  border-radius: 50px;
  padding: 5px;
}

.pokedex-btn-navigation {
  display: block;
  width: 30px;
  height: 30px;
  background-color:rgb(59, 58, 68);
  border-color: gray;
}

.btns-group {
  display: flex;
}

.up {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  border-bottom: none;
}

.down {
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  border-top: none;
}

.left {
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  border-right: none;
}

.right {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  border-left: none;
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