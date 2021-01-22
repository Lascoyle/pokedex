<template>
    <div id="pokedex">
        <div id="pokedex-title-container">
            <h3 id="pokedex-title">This my Pokedex</h3>
        </div>
        <pokedex-screen></pokedex-screen>
        <pokedex-search></pokedex-search>
    </div>
</template>

<script>
import PokedexScreen from './PokedexScreen.vue'
import PokedexSearch from './PokedexSearch.vue'
export default {
    name: 'Pokedex',
    components: {
        PokedexScreen,
        PokedexSearch
    }
}
</script>

<style>
    #pokedex {
        display: flex;
        flex-direction: column;
        align-items: center;
        background: rgb(235, 64, 64);
        min-height: 100vh;
        min-width: 100vw;
        border-radius: 10px;
        border-bottom-right-radius: 50px;
        color: white;
        font-family: sans-serif;
    }

    #pokedex-title-container {
        border-bottom: solid 2px  rgb(189, 57, 57);
        width: 100vw;
        text-align: center;
        margin-bottom: 2%
    }

    #pokedex-title {
        margin-left: 5vw;
        margin-right: 5vw;
        border-right: solid 2px  rgb(189, 57, 57);;
        border-left: solid 2px  rgb(189, 57, 57);;
    }
</style>