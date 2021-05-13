<template>
<div>
   <div class="products-container">
      <div class="product-header">
         <h5 class="product-title">PRODUCT</h5>
         <h5 class="quantity">QUANTITY</h5>
         <h5 class="price">PRICE</h5>
      </div>
      <ul class="products">
      </ul>
      <div class="total__container">
      </div>
   </div>
   <div class="row">
      <div class="colsection">
         <div class="container">
            <div class="row">
               <div class="coldelivery">
                  <h1>BUY RIGHT NOW!!!</h1>
                  <br>
                  <label for="full__name"><em class="fa fa-user"></em> Enter your name:</label>
                  <input type="text" id="full__name" name="firstname" placeholder="Andrei Lungu">
                  <label for="phone"><em class="fa fa-phone"></em> Enter your phone:</label>
                  <input type="text" id="phone" name="phone" placeholder="+37369098833">
                  <label for="email"><i class="fa fa-envelope"></i> Enter your email</label>
                  <input type="email" id="email" name="email" placeholder="Andrei@mail.ru">
                  <label for="address"><em class="fas fa-address-card"></em> Enter your address:</label>
                  <input type="text" id="address" name="address" placeholder="Stefan cel Mare 13/108">
                  <label for="city"><em class="fas fa-city"></em> Enter your city:</label>
                  <input type="text" id="city" name="city" placeholder="Balti">
                  <label for="comment"><em class="fas fa-comment"></em> Enter your comment:</label>
                  <input type="text" id="comment" name="comment" placeholder="Pack the product better please !!!">
                  <div class="row">
                     <div class="coldelivery">
                        <label for="delivery"><em class="fas fa-shipping-fast"></em> Delivery</label>
                        <select id="delivery" name="delivery">
                           <option value="0" selected="selected">Posta Moldovei | 2-3 days | Price: $ 0 </option>
                           <option value="5">DHL | 1-2 days| Price: $ 5</option>
                           <option value="10">UPS Express| 1 day | Price: $ 10</option>
                        </select>
                        <button class="btn1" onclick="goshop()"><em class="fas fa-cart-plus"></em> Continue shopping</button>
                        <button class="btn2" id="order__items"><em class="fa fa-credit-card"></em> Purchase now</button>
                     </div>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </div>
</div>
</template>

<script>
    export default {
        name: "CartPage"
    }
</script>

<style scoped>
.products-container {
	max-width: 680px;
	justify-content: space-around;
	margin: 0 auto;
	margin-top: 50px;
}

.product-header {
	width: 100%;
	max-width: 680px;
	display: flex;
	justify-content: flex-start;
	border-bottom: 4px solid gray;
	margin: 0 auto;
}

.products {
	display: grid;
	grid-template-columns: repeat(1, 1fr);
	grid-template-rows: 1fr;
	grid-column-gap: 0;
	grid-row-gap: 0;
}

.products li {
	display: grid;
	grid-template-columns: repeat(5, 1fr);
	grid-template-rows: 1fr;
	grid-column-gap: 0;
	grid-row-gap: 0;
}

.product-header {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	grid-template-rows: 1fr;
	grid-column-gap: 0;
	grid-row-gap: 0;
}

.remove__btn {
	margin-left: -15px;
	grid-area: 1 / 1 / 2 / 2;
}

.product__img {
	margin-left: 25px;
	grid-area: 1 / 1 / 2 / 3;
}

.product__name {
	grid-area: 1 / 2 / 2 / 4;
}

.product__price {
	grid-area: 1 / 5 / 2 / 6;
}

.product__quantity {
	grid-area: 1 / 4 / 2 / 5;
}

.product__img img {
	width: 65px;
}

.basketTotalContainer {
	display: flex;
	justify-content: flex-end;
	width: 100%;
	padding: 10px 0;
}

.basketTotalTitle {
	width: 30%;
}

.basketTotal {
	width: 10%;
}

.product-title {
	display: flex;
	margin-left: 150px;
	justify-content: flex-start;
}

.quantity {
	display: flex;
	margin-left: 200px;
	justify-content: flex-start;
}

.price {
	display: flex;
	margin-left: 70px;
	justify-content: flex-start;
}

@media screen and (max-width: 620px) {
	.product__name {
		margin-left: 15px;
		grid-area: 1 / 1 / 2 / 4;
	}
	.product__img img {
		display: none;
	}
	.basketTotalContainer {
		display: flex;
		margin-left: 50px;
		width: 100%;
		padding: 10px 0;
	}
	.basketTotal {
		width: fit-content;
	}
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

.container {
	display: flex;
	justify-content: center;
	flex-wrap: wrap;
	margin-top: 50px;
	padding-bottom: 100px;
}

.row {
	display: -ms-flexbox;
	display: flex;
	-ms-flex-wrap: wrap;
	flex-wrap: wrap;
	margin: 0 -16px;
}

.coldelivery {
	-ms-flex: 50%;
	flex: 50%;
}

.colsection {
	-ms-flex: 75%;
	flex: 75%;
}

.coldelivery,
.colsection {
	padding: 0 16px;
}

input[type="text"],
select {
	width: 100%;
	margin-bottom: 20px;
	padding: 12px;
	border: 1px solid #ccc;
	border-radius: 3px;
}

input[type="email"],
select {
	width: 100%;
	margin-bottom: 20px;
	padding: 12px;
	border: 1px solid #ccc;
	border-radius: 3px;
}

label {
	margin-bottom: 10px;
	display: block;
}

.btn1 {
	background-color: rgb(166, 0, 0);
	color: white;
	padding: 12px;
	margin: 10px 0;
	border: none;
	width: 100%;
	border-radius: 3px;
	cursor: pointer;
	font-size: 17px;
}

.btn2 {
	background-color: rgb(166, 0, 0);
	color: white;
	padding: 12px;
	margin: 10px 0;
	border: none;
	width: 100%;
	border-radius: 3px;
	cursor: pointer;
	font-size: 17px;
}

.btn1:hover {
	background-color: #949494;
}

.btn2:hover {
	background-color: #949494;
}

hr {
	border: 1px solid lightgrey;
}

@media (max-width: 800px) {
	.row {
		flex-direction: column-reverse;
	}
}
</style>