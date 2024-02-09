<script>
import PokemonCard from '../PokemonCard.vue';
import { store } from '../../data/store.js';
export default {
    name: 'PokemonList',
    data: () => ({
        store
    }),
    components: { PokemonCard }
}
</script>

<template>
    <section id="pokemon" class="my-5">

        <div class="pokedex">
            <PokemonCard v-for="pokemon in store.pokemons" :key="pokemon._id" :image-url="pokemon.imageUrl"
                :name="pokemon.name" :number="pokemon.number" :type1="pokemon.type1" />
        </div>


    </section>
</template>

<style lang="scss" scoped>
.pokedex {
    display: flex;
    flex-wrap: wrap;
}

.pokedex>* {
    flex-basis: calc(100% / 5);
}
</style>