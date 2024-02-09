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
    <section id="pokemon">

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
    background-color: #565b60;
    padding: 10px;
}

.pokedex>* {
    flex-basis: calc(100% / 5);
}

section {
    background-color: white;
    padding: 20px;
    border-radius: 20px;
}
</style>