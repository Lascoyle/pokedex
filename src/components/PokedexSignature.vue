<template>
  <div>
    <h1 id="pokedex-signature"><span id="pokedex-author">Lascoyle</span><span id="pokedex-brand">Poke Gamedex</span><span id="pokedex-trademark">TM</span></h1>
  </div>
</template>

<script>
export default {
    name: "PokedexSignature"
}
</script>

<style>
@font-face {
    font-family: 'snes';
    src: url('../assets/fonts/snes-font/SnesItalic-1G9Be.ttf') format('truetype');
}

@font-face {
    font-family: 'superfami';
    src: url('../assets/fonts/super-famifont-font/SuperFamifont-Bgmw.ttf') format('truetype');
}

#pokedex-signature {
  align-self: flex-start;
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  margin-left: 5%;
  margin-top: 3px;
  color: rgb(59, 58, 68);
  width: 54%;
}

#pokedex-author {
  font-family: 'superfami', sans-serif;
  font-size: 1rem;
}

#pokedex-brand {
  font-family: 'snes', sans-serif;
  font-size: 2.8rem;
}

#pokedex-trademark {
  font-size: 1rem;
}
</style>