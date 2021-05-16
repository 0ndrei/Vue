<template>
    <section>
        <div class="products-container">
            <div class="product-header">
                <h5 class="product-title">PRODUCT</h5>
                <h5 class="quantity">QUANTITY</h5>
                <h5 class="price">PRICE</h5>
            </div>
            <ul class="products">
                <CartItem
                        :key="product.id"
                        :product_data="product"
                        v-for="product in CART"/>
            </ul>
        </div>
    </section>
</template>

<script>
    import CartItem from "./CartItem";
    import {mapGetters} from "vuex";
    export default {
        name: "CartPage",
        components : {
            CartItem
        },
        computed: mapGetters(['CART'])
    }
</script>

<style scoped>
    section {
        margin-top: 5%;
    }
    .products-container {
        max-width: 680px;
        justify-content: space-around;
        margin: 0 auto;
        margin-top: 100px;
    }

    .product-header {
        width: 100%;
        max-width: 680px;
        display: flex;
        justify-content: flex-start;
        border-bottom: 4px solid gray;
        margin: 0 auto;
    }

    .product-header {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: 1fr;
        grid-column-gap: 0;
        grid-row-gap: 0;
    }

.products {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: 1fr;
        grid-column-gap: 0;
        grid-row-gap: 0;
    }

    .product-title {
        display: flex;
        margin-left: 150px;
        justify-content: flex-start;
    }
    .quantity {
        display: flex;
        margin-left: 210px;
        justify-content: flex-start;
    }
    .price {
        display: flex;
        margin-left: 70px;
        justify-content: flex-start;
    }

    @media screen and (max-width: 620px) {
        .product-title {
            display: flex;
            margin-left: 70px;
            justify-content: flex-start;
        }
        .quantity {
            display: flex;
            margin-left: 100px;
            justify-content: flex-start;
        }
        .price {
            display: flex;
            margin-left: 7px;
            justify-content: flex-start;
        }
    }
</style>