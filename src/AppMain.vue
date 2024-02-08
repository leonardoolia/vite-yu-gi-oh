<script>
import PokemonList from './components/pokemons/PokemonList.vue';
export default {
    name: 'AppMain',
    components: { PokemonList }
}
</script>

<template>
    <main class="container">
        <PokemonList />
    </main>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>