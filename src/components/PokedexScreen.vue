<template>
    <div id="pokedex-screen">
        <div id="pokedex-screen-frame">
            <div id="pokedex-screen-frame-style">
                <div class="pokedex-screen-frame-lines left-lines"></div>
                <p id="pokedex-screen-frame-text">App made thanks to PokéAPI</p>
                <div class="pokedex-screen-frame-lines right-lines"></div>
            </div>
            <div id="pokedex-screen-image">
                <div id="pokedex-screen-image-content">
                    <pokedex-search></pokedex-search>
                    <pokedex-pokemon></pokedex-pokemon>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import PokedexPokemon from './PokedexPokemon.vue'
import PokedexSearch from './PokedexSearch.vue'
export default {
    name: 'PokedexScreen',
    components: {
        PokedexSearch,
        PokedexPokemon
    }
}
</script>

<style>
@font-face {
    font-family: 'gameboy';
    src: url('../assets/fonts/early_gameboy/Early GameBoy.ttf') format('truetype');
}

@font-face {
    font-family: 'pokemon';
    src: url('../assets/fonts/pokemon-gb-font/PokemonGb-RAeo.ttf') format('truetype');
}

#pokedex-screen {
    align-self: center;
    width: 90vw;
    height: 45vh;
    font-family: 'pokemon', sans-serif;
}

#pokedex-screen-frame {
    background-color:rgb(59, 58, 68);
    border-radius: 15px;
    border-bottom-right-radius: 40px;
    padding: 5%;
    width: inherit;
    height: inherit;
}

#pokedex-screen-frame-style {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.pokedex-screen-frame-lines {
    height: 8px;
    width: 20px;
    border-top: pink solid 2px;
    border-bottom: lightblue solid 2px;
}

#pokedex-screen-frame-text {
    font-family: sans-serif;
    text-transform: uppercase;
    font-size: 0.9rem;
    color: rgb(120, 122, 131);
}

.left-lines {
    width: 40%
}

.right-lines {
    width: 10%;
}

#pokedex-screen-image {
    background-color:rgb(177, 199, 149);
    border-radius: 5px;
    width: 75%;
    height: 85%;
    margin: auto;
    margin-top: 10px;
    color: rgb(0, 92, 0);
    overflow-y: scroll;
}

#pokedex-screen-image-content {
    height: 100%;
}
</style>