<template>
    <section>
        <Header/>
        <CartPage/>
        <TotalContainer/>
    </section>
</template>

<script>
    import Header from '@/components/views/header/Header'
    import CartPage from '@/components/views/site-page/cart-main/CartPage';
    import TotalContainer from '@/components/views/site-page/cart-main/TotalContainer';

    export default {
        name: "MainPage",
      components: {
    Header, CartPage, TotalContainer
  },
};
</script>

<style scoped>

</style>