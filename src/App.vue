<script>
import AppHeader from './AppHeader.vue';
import AppMain from './AppMain.vue';
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
import { store } from './data/store';
export default {
  name: 'Pokedex',
  components: { AppHeader, AppMain },

  created() {
    axios.get(endpoint).then(res => {
      store.pokemons = res.data.docs;
    }).catch(err => { console.error(err) })
  }

}
</script>

<template>
  <div class="poke-container">
    <AppHeader />
    <AppMain />
  </div>
</template>

<style lang="scss">
.poke-container {
  background-color: #b71b1b;
}
</style>