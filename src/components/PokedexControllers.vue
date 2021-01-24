<template>
  <div id="pokedex-controllers">
      <pokedex-btn-navigations></pokedex-btn-navigations>
      <pokedex-btn-options></pokedex-btn-options>
      <pokedex-btn-actions></pokedex-btn-actions>
  </div>
</template>

<script>
import PokedexBtnActions from './PokedexBtnActions.vue'
import PokedexBtnNavigations from './PokedexBtnNavigations.vue'
import PokedexBtnOptions from './PokedexBtnOptions.vue'
export default {
    name: 'PokedexControllers',
    components: {
        PokedexBtnNavigations,
        PokedexBtnOptions,
        PokedexBtnActions
    }
}
</script>

<style>
    #pokedex-controllers {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        align-self: center;
        width: 90vw;
        height: 25vh;
        margin-top: 20px;
    }
</style>