<template>
<div>
   <div class="containers">
      <h1>Products</h1>
      <img class="imgnote" src="https://api.scoaladebani.ro/storage/73/8-produs-creditare.png" alt="">
      <section class="categories">
         <div class="card" id="cardItems">
            <ProductItemPage
               :key="product.id"
               :product_data="product"
               @addToCart="showResult"
               v-for="product in PRODUCTS"
               />
         </div>
      </section>
   </div>
</div>
</template>

<script>
import {mapActions, mapGetters} from "vuex";
import ProductItemPage from "./ProductItemPage"

export default {
    name: "Product",
    components: {
        ProductItemPage
    },
    methods: {
        ...mapActions(['GET_PRODUCTS', 'ADD_CART', 'INCREASE_QUANTITY']),
        showResult(product) {
            const currProduct = {
                ...product,
                quantity: 1
            };

            if (this.$cart.inCart(this.CART, product)) this.INCREASE_QUANTITY(product);
            if (!this.$cart.inCart(this.CART, product)) this.ADD_CART(currProduct);

        }
    },
    computed: mapGetters(['PRODUCTS', 'CART']),
    async mounted() {
        await this.GET_PRODUCTS();
    }
};
</script>

<style scoped>
.categories {
	margin-top: 25px;
}

.title-container {
	justify-content: space-between;
	background: white;
	padding: 1rem 0.5rem;
}

.title {
	font-size: 2rem;
	background: white;
	text-align: center;
}

.containers {
	margin: 17%;
	margin-top: 10px;
}

.card {
	display: grid;
	grid-template-columns: auto auto;
	grid-gap: 1px;
	text-align: center;
	font-family: sans-serif;
}

.item-container {
	background: white;
	position: relative;
	background: white;
	padding: 15px 12px;
	position: relative;
}

.item-container:hover {
	background: #d4d4d4;
	transition: all 0.7s ease-in-out;
}

.item-container:hover .card-img {
	transform: scale(1.1);
	transition: all 0.7s ease-in-out;
}

.card-item {
	cursor: pointer;
}

.card-img {
	position: relative;
	max-width: 100%;
	max-height: 8rem;
	text-align: center;
}

.item-name {
	text-align: center;
	font-weight: bold;
	color: rgb(166, 0, 0);
	margin-top: 1rem;
	font-size: 0.95rem;
}

.item-name-index {
	text-align: center;
	font-weight: bold;
	color: black;
	margin-top: 1rem;
	font-size: 0.95rem;
}

.item-description {
	text-align: left;
	color: rgb(0, 0, 0);
	margin-top: 1rem;
	font-size: 0.95rem;
}

.add-to-cart {
	font-size: 1.5rem;
	color: rgb(166, 0, 0);
	position: absolute;
	bottom: 1rem;
	right: 0.8rem;
	cursor: pointer;
	opacity: 0;
}

.item-container:hover .add-to-cart {
	transition: all 0.7s ease-in-out;
	opacity: 1;
}

.item-price {
	color: rgb(221, 0, 0);
	text-align: left;
	margin-top: 0.5rem;
}

.imgnote {
	width: 100%;
}

@media only screen and (max-width: 1790px) {
	.footer {
		margin-top: 0%;
	}
	.containers {
		margin: 0;
	}
}

@media only screen and (min-width: 800px) {
	.card {
		grid-template-columns: repeat(4, 1fr);
	}
}

@media only screen and (max-width: 800px) {
	.items-detail {
		display: block;
		width: 70vw;
		height: 70vh;
		padding: 0 4.5rem;
	}
	#details-img {
		width: 8rem;
		height: 9rem;
	}
	#detail-title {
		font-size: 1.7rem;
		margin-top: 0rem;
	}
	#detail-price,
	#delievery {
		margin-top: 0.5rem;
	}
	#spec,
	.items-detail ul {
		display: none;
	}
	.image-container {
		padding: 1rem;
		margin-top: 1rem;
	}
	.containers {
		margin: 0;
	}
}
</style>