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
        <div class="row row-cols-5 g-4">
            <div class="col">
                <PokemonCard v-for="pokemon in store.pokemons" :key="pokemon._id" :image-url="pokemon.imageUrl"
                    :name="pokemon.name" :number="pokemon.number" :type1="pokemon.type1" />
            </div>

        </div>
    </section>
</template>

<style></style>