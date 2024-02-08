<script>
import PokemonCard from '../PokemonCard.vue';
import { store } from '../../data/store';
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
                <PokemonCard v-for="pokemon in pokemons" :key="pokemon._id" :image-url="pokemon.imageUrl" />
            </div>

        </div>
    </section>
</template>

<style></style>