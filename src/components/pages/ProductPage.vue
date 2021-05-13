<template>
    <section>
        <Header/>
        <ProductPage/>
        <Footer/>
    </section>
</template>

<script>
    import Header from '@/components/views/header/Header'
    import ProductPage from '@/components/views/site-page/product-main/Product-page'
    import Footer from "@/components/views/footer/Footer";

    export default {
        name: "MainPage",
        components : {
            Header, ProductPage, Footer
        }
    }
</script>

<style scoped>

</style>