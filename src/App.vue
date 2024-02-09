<script>
import AppHeader from './AppHeader.vue';
import AppMain from './AppMain.vue';
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
const apiUri = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
import { store } from './data/store';
export default {
  name: 'Pokedex',
  data: () => ({
    types: [
      "Bug",
      "Dark",
      "Dragon",
      "Electric",
      "Fairy",
      "Fighting",
      "Fire",
      "Flying",
      "Ghost",
      "Grass",
      "Ground",
      "Ice",
      "Normal",
      "Poison",
      "Psychic",
      "Rock",
      "Steel",
      "Water"
    ]
  }),
  components: { AppHeader, AppMain },
  methods: {
    filterPokemon(type) {
      const endpoint = `${apiUri}?eq[type1]=${type}`;
      axios.get(endpoint).then(res => {
        store.pokemons = res.data.docs;
      }).catch(err => { console.error(err) })
    }
  },

  created() {
    axios.get(endpoint).then(res => {
      store.pokemons = res.data.docs;
    }).catch(err => { console.error(err) })
  }

}
</script>

<template>
  <div class="poke-container">
    <AppHeader :types="types" @type-change="filterPokemon" />
    <AppMain />
  </div>
</template>

<style lang="scss">
.poke-container {
  background-color: #b71b1b;
}
</style>