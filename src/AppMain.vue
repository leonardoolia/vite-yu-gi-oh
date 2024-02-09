<script>
import PokemonList from './components/pokemons/PokemonList.vue';
export default {
    name: 'AppMain',
    components: { PokemonList }
}
</script>

<template>
    <main>
        <div class="container">
            <PokemonList />
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use './assets/scss/style.scss';
</style>