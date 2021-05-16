<template>
    <section>
        <Header/>
        <CartPage/>
        <PriceContainer/>
    </section>
</template>

<script>
    import Header from '@/components/views/header/Header'
    import CartPage from '@/components/views/site-page/cart-main/CartPage';
    import PriceContainer from '@/components/views/site-page/cart-main/PriceContainer';

    export default {
        name: "MainPage",
      components: {
    Header, CartPage, PriceContainer
  },
};
</script>

<style scoped>

</style>