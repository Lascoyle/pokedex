<template>
   <div id="pokedex-search">
        <h2 id="pokedex-search-title">Search A Pokemon</h2>
        <div id="pokedex-search-question-mark">?</div>
        <form id="pokedex-search-form" action="GET">
          <input id="pokemon-input" type="text" placeholder="Enter a pokemon..." v-model="pokemonName">
          <div id="keyboard">
              <span class="keyboard-input" v-for="(letter, index) in alphabetLetters" :key="index" @click="enterLetter(letter)">
                  {{ letter }}
              </span>
          </div>
       </form>
   </div>
</template>

<script>
export default {
    name: 'PokedexSearch',
    data() {
        return {
            alphabetLetters: [...'abcdefghijklmnopqrstuvwxyz'],
            pokemonLetters: [],
            pokemonName: "",
        }
    },

    methods: {
        enterLetter(letter) {
            this.pokemonLetters.push(letter);
            this.pokemonName = this.pokemonLetters.join('');
            this.pokemonName.toLowerCase()
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
    background: ;
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
}

.keyboard-input {
    display: inline-block;
    padding: 5px;
}
</style>