<template>
    <section>
        <Header/>
        <Product/>
        <Footer/>
    </section>
</template>

<script>
    import Header from '@/components/views/header/Header'
    import Product from '@/components/views/site-page/product-main/Product'
    import Footer from "@/components/views/footer/Footer";

    export default {
        name: "ProductPage",
        components : {
            Header, Product, Footer
        }
    }
</script>

<style scoped>

</style>