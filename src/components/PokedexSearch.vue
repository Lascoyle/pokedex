<template>
   <div id="pokedex-search">
        <h2 id="pokedex-search-title">Search A Pokemon</h2>
        <div id="pokedex-search-question-mark">?</div>
        <div id="pokedex-search-form">
          <input id="pokemon-input" type="text" placeholder="Enter a pokemon..." v-model="pokemonName">
          <div id="keyboard">
              <div id="keyboard-inputs">
                  <span class="keyboard-input" v-for="(letter, index) in alphabetLetters" :key="index" @click="enterLetter(letter)">
                      {{ letter }}
                  </span>
                  <span class="keyboard-input erase-input" @click="eraseLetter()">🠔</span>
                  <span class="keyboard-input erase-name" @click="eraseName()">⌫</span>
                  <button @click="sendPokemonName(pokemonName)">Enter</button>
              </div>
          </div>
       </div>
   </div>
</template>

<script>
import { bus } from "../main";
export default {
    name: 'PokedexSearch',
    data() {
        return {
            alphabetLetters: [...'abcdefghijklmnopqrstuvwxyz'],
            pokemonLetters: [],
            pokemonName: ""
        }
    },

    methods: {
        enterLetter(letter) {
            this.pokemonLetters.push(letter);
            this.pokemonName = this.pokemonLetters.join('');
            this.pokemonName.toLowerCase();
        },

        eraseLetter() {
            this.pokemonLetters.pop();
            this.pokemonName = this.pokemonLetters.join('');
        },

        eraseName() {
            this.pokemonLetters = [];
            this.pokemonName = "";
        },
        sendPokemonName(pokemonName) {
            bus.$emit("sendPokemonName", pokemonName);
            let pokedexSearch = document.getElementById('pokedex-search');
            pokedexSearch.style.display = "none";
        }
    }
}
</script>

<style>
#pokedex-search {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

#pokedex-search-form {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
}

#pokedex-search-title {
    padding: 3%;
    width: 100%;
    border-radius: 5px;
    border: double 8px rgb(0, 92, 0);
    background: inherit;
    color: white;
    font-weight: bold;
    font-family: 'gameboy';
    color: rgb(0, 92, 0);
    font-size: 1rem;
    text-align: center;
}

#pokedex-search-question-mark {
    text-align: center;
    font-size: 3rem;
}

#pokemon-input {
    background-color:rgb(177, 199, 149);
    border: solid 3px rgb(0, 92, 0);
    border-radius: 5px;
    padding: 3%;
    font-family: 'gameboy';
    color: rgb(0, 92, 0);
    font-size: 1rem;
    padding-left: 15px;
}

#keyboard {
    padding: 3%;
    border: solid 3px rgb(0, 92, 0);
    border-radius: 5px;
    font-size: 1.2rem;
    display: flex;
    justify-content: center;
}
.keyboard-input {
    display: inline-block;
    padding: 5px;
}

.keyboard-input:hover {
    cursor: pointer;
}
</style>