<template>
<div>
            <div class="item-container" data-id="1">
               <div class="card-item">
				<p class="item-name">{{product_data.name}}</p>
                  <img :src="require(`../../../../../static/img/${product_data.tag}.png`)" alt="img" class="card-img">
                  <p class="item-description">{{product_data.description}}</p>
               </div>
               <h3 class="item-price"> Price : <span class="item-price-value">{{product_data.price}}</span> $ </h3>
               <a @click="$emit('addToCart', product_data)"><em class="fas fa-shopping-basket add-to-cart"></em></a>
            </div>
         </div>
</template>

<script>
export default {
    name: "ProductItemPage",
	props: {
            product_data: {
                type: Object,
                default: () => ({})
            }
        }
    }
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
	padding: 5px;
	text-align: center;
  font-weight: bold;
  color: rgb(166, 0, 0);
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