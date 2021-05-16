<template>
    <div>
        <div class="total__container">
            <div class="basketTotalContainer">
                <h4 class="basketTotalTitle">Total Price</h4>
                <h4 class="basketTotal">${{$cart.cartSum(CART, parseInt(shippingPrice))}}</h4>
            </div>
        </div>

  <div class="containers">
        <div class="row">
            <div class="colsection">
            <section class="form-container">
                        <div class="container">
                            <div class="row">
                                <div class="coldelivery">
                                    <h1>BUY RIGHT NOW!!!</h1>
                                    <br>
                                    <label for="full__name"><em class="fa fa-user"></em> Enter your name:</label>
                                    <input type="text" id="full__name" name="firstname" placeholder="Andrei Lungu" v-model="full__name"/>
                                    <label for="phone"><em class="fa fa-phone"></em> Enter your phone:</label>
                                    <input type="text" id="phone" name="phone" placeholder="+37369098833" v-model="phone"/>
                                    <label for="email"><i class="fa fa-envelope"></i> Enter your email</label>
                                    <input type="email" id="email" name="email" placeholder="Andrei@mail.ru" v-model="email"/>
                                    <label for="address"><em class="fas fa-address-card"></em> Enter your address:</label>
                                    <input type="text" id="address" name="address" placeholder="Stefan cel Mare 13/108" v-model="address"/>
                                    <label for="city"><em class="fas fa-city"></em> Enter your city:</label>
                                    <input type="text" id="city" name="city" placeholder="Balti" v-model="city">
                                    <label for="comment"><em class="fas fa-comment"></em> Enter your comment:</label>
                                    <input type="text" id="comment" name="comment" placeholder="Pack the product better please !!!">
                                    <div class="row">
                                        <div class="coldelivery">
                                            <label for="delivery"><em class="fas fa-shipping-fast"></em> Delivery</label>
                                            <select id="delivery" name="delivery"  v-model="shippingPrice">
                                                <option value="0" selected="selected">Posta Moldovei | 2-3 days | Price: $ 0 </option>
                                                <option value="5">DHL | 1-2 days| Price: $ 5</option>
                                                <option value="10">UPS Express| 1 day | Price: $ 10</option>
                                            </select>
                                            <button class="btn1" @click="goshop()"><em class="fas fa-cart-plus"></em> Continue shopping</button>
                                            <button class="btn2" id="validate" @click="validateForm"><em class="fa fa-credit-card"></em> Purchase now</button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
            </section>
            </div>
        </div>
  </div>
        
    </div>
</template>

<script>
    import {mapActions, mapGetters} from "vuex";

    export default {
        name: "PriceContainer",
        data: () => ({
            city: '',
            shippingPrice: 0,
            address: '',
            phone: '',
            full__name: '',
            email: '',
        }),
        computed: mapGetters(["CART"]),
        methods: {
            ...mapActions(['CLEAR__CART']),
            validateForm() {

                const full__nameRegexp = /^[a-zA-Z ]{2,30}$/;
                if (!(new RegExp(full__nameRegexp).test(this.full__name))) {
                    console.log("Wrong Name");
                    return;
                }

                const phoneRegexp = /^[+373|373]*[0]*[0-9]{7,8}$/;
                if (!(new RegExp(phoneRegexp).test(this.phone))) {
                    console.log("Wrong Phone Number");
                    return;
                }


                const emailRegexp = /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;
                if (!new RegExp(emailRegexp).test(this.email)) {
                    console.log("Wrong Email");
                    return;
                }

                const addressRegexp = /^[a-zA-Z0-9\s,'-]{4,}$/;
                if (!(new RegExp(addressRegexp).test(this.address) && (this.address.length < 20))) {
                    console.log("Wrong Address");
                    return;
                }

                const cityRegexp = /^[a-zA-z] ?([a-zA-z]|[a-zA-z] )*[a-zA-z]$/;
                if (!(new RegExp(cityRegexp).test(this.city))) {
                    console.log("Wrong City");
                    return;
                }



                localStorage.setItem("full__name", this.full__name);
                localStorage.setItem("phone", this.phone);
                localStorage.setItem("email", this.email);
                localStorage.setItem("address", this.address);
                localStorage.setItem("city", this.city);
                localStorage.setItem("orderedItems", JSON.stringify(this.CART));
                localStorage.setItem("shippingPrice", this.shippingPrice.toString());

                this.CLEAR__CART();
                this.shippingPrice = 0;

                alert("Your order has been taken over by the administrator and you will be called soon.");
            }
        },
    }
</script>

<style scoped>
.basketTotalContainer {
  display: flex;
  justify-content: flex-end;
  width: 60%;
  padding: 10px 0;
}

.basketTotalTitle {
    display: flex;
  justify-content: flex-start;
  width: 100px;
}

.basketTotal {
    display: flex;
  justify-content: flex-start;
}

.categories {
  margin-top: 25px;
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

@media screen and (max-width: 620px) {
        .basketTotalContainer {
            display: flex;
            justify-content: center;
            margin-left: 50px;
            width: 100%;
            padding: 10px 0;
        }

        .basketTotal {
            width: fit-content;
        }


    }
</style>