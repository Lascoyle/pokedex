<template>
    <div>
        <div id="pokemon-card" v-if="pokemonCalled === true">
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
            <div id="pokemon-call-to-scroll">▼ Learn more</div>
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
</template>

<script>
import axios from 'axios'

import { bus } from "../main";

export default {
    name: "PokedexPokemon",
    data() {
        return {
            pokemon: {},
            sprite: "",
            pokemonQuery: "",
            pokemonCalled: false
        }
    },

    created() {
        bus
        .$on('sendPokemonName', (data) => {
            this.pokemonQuery = data;

        axios
        .get(`https://pokeapi.co/api/v2/pokemon/${this.pokemonQuery}`)
        .then(response =>(this.pokemon = response.data, this.sprite = response.data.sprites.front_default, console.log(response)))

        this.pokemonCalled = true;
        });
    },
}
</script>

<style>
#pokemon-card {
    height: 90%;
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

#pokemon-call-to-scroll {
    font-size: 1rem;
    text-align: center;
    margin-top: 5%;
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