<template>
    <div id="pokedex">
        <div id="pokedex-title-container">
            <h3 id="pokedex-border"></h3>
        </div>
        <pokedex-screen></pokedex-screen>
        <pokedex-signature></pokedex-signature>
        <pokedex-controllers></pokedex-controllers>
        <pokedex-speaker></pokedex-speaker>
    </div>
</template>

<script>
import PokedexControllers from './PokedexControllers.vue'
import PokedexScreen from './PokedexScreen.vue'
import PokedexSignature from './PokedexSignature.vue'
import PokedexSpeaker from './PokedexSpeaker.vue'

export default {
    name: 'Pokedex',
    components: {
        PokedexScreen,
        PokedexSignature,
        PokedexControllers,
        PokedexSpeaker
    }
}
</script>

<style>
    #pokedex {
        display: flex;
        flex-direction: column;
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

    #pokedex-border {
        margin-left: 5vw;
        margin-right: 5vw;
        height: 20px;
        border-right: solid 2px  rgb(189, 57, 57);
        border-left: solid 2px  rgb(189, 57, 57);
    }
</style>