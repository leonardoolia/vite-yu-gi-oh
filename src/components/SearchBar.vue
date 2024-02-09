<script>
export default {
    name: 'SearchBar',
    data: () => ({
        selectedOption: ''
    }),
    props: {
        options: Array
    },
    emits: ['option-change']
}
</script>

<template>
    <select v-model="selectedOption" @change="$emit('option-change', selectedOption)">
        <option value="">All</option>
        <option v-for="(option, i) in options" :key="i" :value="option">{{ option }}</option>
    </select>
</template>

<style></style>