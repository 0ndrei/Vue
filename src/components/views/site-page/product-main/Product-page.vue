<template>
<main id="main">
   <div class="containers">
      <h1>Products</h1>
      <img class="imgnote" src="https://api.scoaladebani.ro/storage/73/8-produs-creditare.png" alt="">
      <!-- Notebooks -->
      <section class="categories">
         <div class="title-container">
         </div>
         <div class="card">
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/msi.png')" alt="img" class="card-img">
                  <p class="item-name-index">MSI GF65 Thin Gaming 99SD-252US</p>
               </div>
               <h3 class="item-price">SOON</h3>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/tucano.png')" alt="img" class="card-img">
                  <p class="item-name-index">Tucanoc BACKPACK RAPIDO15.6 ", Blue</p>
               </div>
               <h3 class="item-price">SOON</h3>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/m313.png')" alt="img" class="card-img">
                  <p class="item-name-index">MARVO "M313", 800-6400 DPI </p>
               </div>
               <h3 class="item-price">SOON</h3>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/970evo.png')" alt="img" class="card-img">
                  <p class="item-name-index">SSD 1.0TB Samsung 970 EVO</p>
               </div>
               <h3 class="item-price">SOON</h3>
            </div>
         </div>
         <div class="card" id="cardItems">
         </div>
      </section>
   </div>
</main>
</template>

<script>
export default {
    name: "ProductPage"
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