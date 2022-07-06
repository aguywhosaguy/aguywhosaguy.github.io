<script>
    export default {
        data() {
            return {
                ores: [
                    {name: 'coal', av: 275000, cv: 1}
                ]
            }
        }
    }
</script>

<template>
    <form>
        <li v-for="ore in ores" class="grid">
            <label>{{ore.name}}</label>
            <label>{{ore.av}}</label>
            <label>{{ore.cv}}</label>
        </li>
    </form>

</template>

<style lang="scss">
    .tile {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(49, 1fr);
        grid-gap: 1px;
        background-color: #eee;
    }
</style>