<script>
import SearchBar from './components/SearchBar.vue';
export default {
    name: 'AppHeader',
    components: { SearchBar },
    props: {
        types: Array
    },
    emits: ['type-change']
}
</script>

<template>
    <header>
        <div class="container ">
            <div class="button button-blue"></div>
            <div class="button button-red"></div>
            <div class="button button-yellow"></div>
            <div class="button button-green"></div>
        </div>
        <SearchBar class="searchbar" :options="types" @option-change="$emit('type-change', $event)" />
    </header>
</template>

<style lang='scss' scoped>
header {
    min-height: 100px;
    display: flex;
    align-items: center;
    padding: 0 100px 0 100px
}

.searchbar {
    height: 40px;
}

.container {
    display: flex;
    align-items: center;
    gap: 10px
}

.button {
    height: 50px;
    width: 50px;
    border: 3px solid white;
    border-radius: 50%;
}

.button-blue {
    height: 80px;
    width: 80px;
    background-color: #2e2eff;
    background-image: linear-gradient(135deg, white 5px, #2e2eff);
}

.button-red {
    background-color: #ff3030;
    background-image: linear-gradient(135deg, white 5px, #ff3030);
}

.button-yellow {
    background-color: #ffff4f;
    background-image: linear-gradient(135deg, white 5px, #ffff4f);
}

.button-green {
    background-color: #3b9e3b;
    background-image: linear-gradient(135deg, white 5px, #3b9e3b);
}
</style>