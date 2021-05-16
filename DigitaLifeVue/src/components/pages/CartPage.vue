<template>
    <section>
        <Header/>
        <CartPage/>
    </section>
</template>

<script>
    import Header from '@/components/views/header/Header'
    import CartPage from '@/components/views/site-page/cart-main/Cart-page'

    export default {
        name: "MainPage",
        components : {
            Header, CartPage
        }
    }
</script>

<style scoped>

</style>