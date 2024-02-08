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
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>