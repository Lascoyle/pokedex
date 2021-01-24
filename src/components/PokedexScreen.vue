<template>
    <div id="pokedex-screen">
        <div id="pokedex-screen-frame">
            <div id="pokedex-screen-frame-style">
                <div class="pokedex-screen-frame-lines left-lines"></div>
                <p id="pokedex-screen-frame-text">App made thanks to PokéAPI</p>
                <div class="pokedex-screen-frame-lines right-lines"></div>
            </div>
            <div id="pokedex-screen-image">
                <div id="pokemon-card">
                    <h1 id="pokemon-identity"><span id="pokemon-name">{{ pokemon.name.toUpperCase() }}</span> <span id="pokemon-identifier">#{{ pokemon.id }}</span></h1>
                    <div id="pokemon-characteristics">
                        <img id="pokemon-image" :src="sprite" alt="Sprite of current pokemon">
                        <div id="pokemon-characteristics-infos">
                            <div id="pokemon-type">
                                <p id="pokemon-type-label">Type:</p>
                                <p id="pokemon-type-value">{{ pokemon.types[0].type.name }}</p>
                            </div>
                            <ul id="pokemon-scale">
                                <li class="pokemon-scale-item">
                                    <p class="pokemon-scale-item-label">Height:</p>
                                    <p class="pokemon-scale-item-value">{{ pokemon.height }}</p>
                                </li>
                                <li class="pokemon-scale-item">
                                    <p class="pokemon-scale-item-label">Weight:</p>
                                    <p class="pokemon-scale-item-value">{{ pokemon.weight }}</p>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div id="pokemon-stats">
                    <h3 id="pokemon-stats-title">Statistics</h3>
                    <ul id="pokemon-stats-list">
                        <li class="pokemon-stat" v-for="(stat, index) in pokemon.stats" :key="index">
                            <span class="pokemon-stat-label">{{ stat.stat.name.toUpperCase() }}:</span>
                            <span class="pokemon-stat-value">{{ stat.base_stat }}</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PokedexScreen',
    props :{
        pokemon: {
            type: Object,
            required: true
        },
        sprite: {
            type: String,
            required: true
        }
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

#pokemon-card {
    height: 100%;
}

#pokemon-identity {
    text-align: center;
    padding: 5px;
    border: double 8px rgb(0, 92, 0);
    border-radius: 5px;
    font-size: 1.3rem;
}

#pokemon-characteristics {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding-bottom: 37px;
}

#pokemon-image {
    display: block;
    margin-top: 30px;
    scale: 1.5;
    filter: sepia(100%) hue-rotate(50deg);
}

#pokemon-type {
    font-size: 1.2rem;
    margin-top: 40px;
    margin-bottom: 20px;
}

.pokemon-scale-item {
    font-size: 1rem;
}

#pokemon-stats {
    font-size: 0.9rem;
    border : solid 2px rgb(0, 92, 0);
    line-height: 20px;
    height: 100%;
}

#pokemon-stats-title {
    border : solid 2px rgb(0, 92, 0);
    padding: 5px;
    padding-left: 10px;
    text-transform: uppercase;
}

#pokemon-stats-list {
    padding: 10px;
}
</style>