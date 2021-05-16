<template>
    <li>
        <div class="remove__btn" @click="REMOVE_PRODUCT(product_data)">
            <em class="fas fa-trash-alt remove__item"></em>
        </div>
        <div class="product__img">
            <img :src="require(`../../../../../static/img/${product_data.tag}.png`)" alt="">
        </div>
        <div class="product__name">
            <span>{{product_data.name}}</span>
        </div>
        <div class="product__quantity">
            <div @click="DECREASE_QUANTITY(product_data)">
                <em class="fas fa-minus-circle decrease__item"></em>
            </div>

            <span>{{product_data.quantity}}</span>
            <div @click="INCREASE_QUANTITY(product_data)">
                <em class="fas fa-plus-circle increase__item"></em>
            </div>

        </div>
        <div class="product__price">
            $<span>{{product_data.price}}</span>
        </div>
    </li>
</template>

<script>
    import {mapActions} from "vuex";

    export default {
        name: "CartItem",
        props: {
            product_data: {
                type: Object,
                default: () => ({})
            }
        },
        methods: mapActions(['REMOVE_PRODUCT', 'INCREASE_QUANTITY', 'DECREASE_QUANTITY'])
    }
</script>

<style scoped>
.products li {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: 1fr;
  grid-column-gap: 0;
  grid-row-gap: 0;
}

.remove__btn {
    margin-top: 5px;
  grid-area: 1 / 1 / 2 / 2;
}


.product__name {
    margin-top: 5px;
  display: flex;
    justify-content: flex-start;
}

.product__price {
    margin-top: 5px;
  display: flex;
  justify-content: center;
}

.product__quantity {
    margin-top: 5px;
    display: flex;
  justify-content: center;

}

.product__img img {
    margin-top: 5px;
  width: 65px;
   display: flex;
  justify-content: center;
}

@media screen and (max-width: 700px) {
  .product__name {
    margin-left: 35px;
    grid-area: 1 / 3 / 2 / 4;
  }

}
@media screen and (max-width: 620px) {
        
    .products li {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr;
  grid-column-gap: 0;
  grid-row-gap: 0;
}
  .product__name {
    margin-left: 35px;
    grid-area: 1 / 1 / 2 / 4;
  }

  .product__img img {
    display: none;
  }
  .product__quantity {
    grid-area: 1 / 2 / 2 / 4;

}
.product__price {
  grid-area: 1 / 3 / 2 / 4;

}
}
@media screen and (max-width: 400px) {
        
    .products li {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr;
  grid-column-gap: 0;
  grid-row-gap: 0;
}
  .product__name {
    margin-left: 35px;
    grid-area: 1 / 1 / 2 / 4;
  }

  .product__img img {
    display: none;
  }
  .product__quantity {
    grid-area: 1 / 2 / 2 / 4;

}
.product__price {
  grid-area: 1 / 3 / 2 / 4;

}
}
</style>