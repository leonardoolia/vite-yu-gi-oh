<script>
export default {
    name: 'PokemonCard',
    props: {
        imageUrl: String,
        name: String,
        number: Number,
        type1: String
    }
}
</script>

<template>
    <div class="pokemon-card text-center p-2">
        <img :src="imageUrl" :alt="name" class="img-fluid rounded-circle mb-3">
        <div>{{ number }}</div>
        <h4>{{ name }}</h4>
        <div>{{ type1 }}</div>
    </div>
</template>

<style></style>