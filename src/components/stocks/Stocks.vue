<template>
    <ul class="stocks">
        <Stock v-for="stock in stocks" :stock="stock"></Stock>
    </ul>
</template>

<script>
import Stock from './Stock'

export default {
    data() {
        return {
            stocks: [
                { id: 1, name: 'BMW', price: 110 },
                { id: 2, name: 'Google', price: 200 },
                { id: 3, name: 'Apple', price: 150 },
                { id: 4, name: 'Twitter', price: 80 }
            ]
        }
    },
    components: {
        Stock
    }    
}
</script>

<style lang="scss" scope>
    .stocks {
        width: 100%;
        max-width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        list-style: none;
    }

    li {
        width: 50%;
    }
</style>