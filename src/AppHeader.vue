<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <div class="container">
            <div class="button button-blue"></div>
            <div class="button button-red"></div>
            <div class="button button-yellow"></div>
            <div class="button button-green"></div>
        </div>
    </header>
</template>

<style lang='scss' scoped>
header {
    min-height: 100px;
    background-color: #b71b1b;
    padding: 10px;
}

.container {
    display: flex;
    align-items: center;
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