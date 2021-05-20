<template>
<main>
   <div class="container-index">
      <div class="left-column">
         <img data-image="red" class="active-index" :src="require('../../../../../static/img/msitop.png')" alt="">
      </div>
      <div class="right-column">
         <div class="index-description">
            <span>notebook</span>
            <h1>MSI GT76 Titan</h1>
            <p>The one that is the most adaptable to change is the one that survive and evolve. Choose the Dragon Spirit
               and evolve with the latest MSI Gaming Laptops equipped with 10th Gen. Intel® Core™ i9 processors (Comet
               Lake H) & latest GeForce® RTX graphics designed for gamers with style. Head first into the New
               Generation.
            </p>
         </div>
         <div class="product-configuration">
            <div class="ssd-config">
               <span>SSD configuration</span>
               <div class="ssd-choose">
                  <button>512GB</button>
                  <button>1T</button>
                  <button>4T</button>
                  <button>10T</button>
               </div>
               <a href="https://www.msi.com/Landing/2020-Gaming-laptops-evolve/nb">How to configure your notebook</a>
            </div>
         </div>
         <div class="index-price">
            <span>SOON</span>
            <a class="cart-btn" @click="goshop()">Go shopping</a>
         </div>
      </div>
   </div>
   <!-- Products waiting -->
   <div class="containers">
      <section class="categories">
         <div class="title-container">
            <hr>
            <h2 class="title">
               Products waiting
            </h2>
            <hr>
         </div>
         <div class="card">
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/msi.png')" alt="img" class="card-img">
                  <p class="item-name-index">MSI GF65 Thin Gaming 9SD-252US</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/tucano.png')" alt="img" class="card-img">
                  <p class="item-name-index">Tucano BACKPACK RAPIDO15.6 ", Blue</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/m313.png')" alt="img" class="card-img">
                  <p class="item-name-index">MARVO "M313", 800-6400 DPI </p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/970evo.png')" alt="img" class="card-img">
                  <p class="item-name-index">SSD 1.0TB Samsung 970 EVO</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
         </div>
      </section>
      <!-- Popular products waiting -->
      <section class="categories">
         <div class="title-container">
            <hr>
            <h2 class="title">
               Popular products waiting
            </h2>
            <hr>
         </div>
         <div class="card">
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/bag3.png')" alt="img" class="card-img">
                  <p class="item-name-index">Xiaomi Simple Casual Backpack</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/asus.png')" alt="img" class="card-img">
                  <p class="item-name-index">NB ASUS 15.6" G512LW</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/mouse4.png')" alt="img" class="card-img">
                  <p class="item-name-index">HYPERX Pulsefire, 400–6200 DPI</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
            <div class="item-container">
               <div class="card-item">
                  <img :src="require('../../../../../static/img/acer.png')" alt="img" class="card-img">
                  <p class="item-name-index">ACER Nitro AN515-55 Obsidian Black</p>
               </div>
               <h3 class="item-price">SOON</h3>
               <button class="buttongotoshop" @click="goshop()">Go shopping</button>
            </div>
         </div>
      </section>
   </div>
</main>
</template>

<script>
export default {
    name: "HomePage",
    methods: {
        goshop() {
            this.$router.push("/products");
        },
    },
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
	background: white;
	transition: all 0.7s ease-in-out;
}

.item-container:hover .card-img {
	transform: scale(1.1);
	transition: all 0.7s ease-in-out;
}

.card-item {
	cursor: pointer;
}

.buttongotoshop {
	background-color: rgb(166, 0, 0);
	border: none;
	border-radius: 15px;
	color: white;
	padding: 5px 20px;
	text-align: center;
	text-decoration: none;
	font-size: 16px;
	margin: 4px 2px;
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

.item-container:hover {
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

.bady-index {
	height: 100%;
	width: 100%;
	margin: 0;
	font-family: "Roboto", sans-serif;
}

.container-index {
	margin-top: 20px;
	max-width: 1200px;
	margin: 0 auto;
	padding: 15px;
	display: flex;
}

.left-column {
	width: 65%;
	position: relative;
}

.right-column {
	width: 35%;
	margin-top: 60px;
}

.left-column img {
	width: 90%;
	position: absolute;
	left: 50px;
	top: 60px;
	opacity: 0;
	transition: all 0.3s ease;
}

.left-column img.active-index {
	opacity: 1;
}

.index-description {
	border-bottom: 1px solid #e1e8ee;
	margin-bottom: 20px;
}

.index-description span {
	font-size: 12px;
	font-weight: bold;
	color: rgb(166, 0, 0);
	letter-spacing: 1px;
	text-transform: uppercase;
	text-decoration: none;
}

.index-description h1 {
	font-weight: 300;
	font-size: 52px;
	color: #43484d;
	letter-spacing: -2px;
}

.index-description p {
	font-size: 16px;
	font-weight: 300;
	color: #86939e;
	line-height: 24px;
}

.cable-config span {
	font-size: 14px;
	font-weight: 400;
	color: #86939e;
	margin-bottom: 20px;
	display: inline-block;
}

.ssd-choose {
	margin-bottom: 20px;
}

.ssd-choose button {
	border: 2px solid #e1e8ee;
	border-radius: 6px;
	padding: 13px 20px;
	font-size: 14px;
	color: #5e6977;
	background-color: #fff;
	cursor: pointer;
	transition: all 0.5s;
}

.ssd-choose button:hover,
.ssd-choose button:active,
.ssd-choose button:focus {
	border: 2px solid #86939e;
	outline: none;
}

.ssd-config {
	border-bottom: 1px solid #e1e8ee;
	margin-bottom: 20px;
}

.ssd-config a {
	color: #358ed7;
	text-decoration: none;
	font-size: 12px;
	position: relative;
	margin: 10px 0;
	display: inline-block;
}

.ssd-config a:before {
	content: "?";
	height: 15px;
	width: 15px;
	border-radius: 50%;
	border: 2px solid rgba(53, 142, 215, 0.5);
	display: inline-block;
	text-align: center;
	line-height: 16px;
	opacity: 0.5;
	margin-right: 5px;
}

.index-price {
	display: flex;
	align-items: center;
}

.index-price span {
	font-size: 26px;
	font-weight: 300;
	color: rgb(221, 0, 0);
	margin-right: 20px;
}

.cart-btn {
	display: inline-block;
	background-color: rgb(166, 0, 0);
	border-radius: 6px;
	font-size: 16px;
	color: #ffffff;
	text-decoration: none;
	padding: 12px 30px;
	transition: all 0.5s;
}

.cart-btn:hover {
	background-color: #949494;
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

@media (max-width: 940px) {
	.container-index {
		flex-direction: column;
		margin-top: 60px;
	}
	.left-column,
	.right-column {
		width: 100%;
	}
	.left-column img {
		width: 300px;
		right: 0;
		top: -65px;
		left: initial;
	}
}

@media (max-width: 690px) {
	.left-column img {
		width: 220px;
		top: -68px;
	}
}
</style>