<template>
    <li class="stock">
        <div class="stock__inner">
            <header class="stock__head">
                <h6 class="stock__title">{{ stock.name }}</h6>
                <span class="stock__price">(Price: {{ stock.price }})</span>
            </header>

            <div class="stock__body">
                <div class="stock__body-inner">
                    <input type="number" placeholder="Qty" v-model="quantity">

                    <a  class="btn btn-primary" 
                        @click="buyStock" 
                        :disabled="quantity <= 0 || !Number.isInteger(quantity)">
                        Buy
                    </a>
                </div>
            </div>
        </div>
        <!-- Features -->
        <!-- Name of the Stock / Price / Input field / Buy Button  -->
        <!-- If the input is empty don't allow the user to buy -->
        <!-- number > 0 -->
    </li>
</template>

<script>
export default {
    props: ['stock'],
    data() {
        return {
            quantity: 0
        }
    },
    methods: {
        buyStock() {
            const order = {
                stockId: this.stock.id,
                stockPrice: this.stock.price,
                stockQty: this.quantity
            };

            console.log(order)
            this.quantity = 0;
        }
    }
}
</script>

<style lang="scss" scope>
    .stock {
        .stock__inner {
            border: 1px solid grey;
            padding: 10px;
            background: lightblue;
        }

        .stock__head {
            display: flex;
            align-items: center;
        }

        .stock__title {
            font-size: 18px;
        }

        .stock__price {
            font-size: 12px;
            margin-left: 10px;
        }

        .stock__body {
            &-inner {
                display: flex;
                justify-content: space-between;
            }
        }
    }
</style>