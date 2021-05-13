<template>
    <header>
      <!--Navbar-->
      <div class="topnav" id="myTopnav">
         <a @click="checkCurrentRoute($router, '/')" class="active"><em class="fa fa-home"></em> Home</a>
         <a @click="checkCurrentRoute($router, '/products')"><em class="fa fa-cart-arrow-down"></em> Products</a>
         <a @click="checkCurrentRoute($router, '/credit')"><em class="fa fa-percent"></em> Credit</a>
         <a @click="checkCurrentRoute($router, '/contact')"><em class="fa fa-phone"></em> Contact</a>
         <a @click="checkCurrentRoute($router, '/cart')" class="cart"><em class="fa fa-shopping-basket"> Cart </em><span id="cartValue">
               0</span></a>
         <a href="javascript:void(0);" class="icon" onclick="myFunction()">
            <em class="fa fa-bars"></em>
         </a>
      </div>
   </header>
</template>

<script>
    import {checkCurrentRoute} from "@/router/routeCheck";

    export default {
        name: "Header",
        data: () => ({
            isToggled: false,
            checkCurrentRoute
        }),
        methods : {
            toggleMenu() {
                this.isToggled = !this.isToggled;
            }
        }
    }
</script>

<style scoped>
    body {
  margin: 0;
  font-family: Arial;
}

.topnav {
  overflow: hidden;
  background-color: rgb(166, 0, 0);
}

.topnav a {
  cursor: pointer;
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav .icon {
  display: none;
}

.topnav a:hover {
  background-color: #949494;
  color: white;
}

@media screen and (max-width: 650px) {
  .topnav a:not(:first-child) {
    display: none;
  }
  .topnav a.icon {
    float: right;
    display: block;
  }
}

@media screen and (max-width: 650px) {
  .topnav.responsive {
    position: relative;
  }
  .topnav.responsive .icon {
    position: absolute;
    right: 0;
    top: 0;
  }
  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
  }
}
</style>