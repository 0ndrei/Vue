<template>
    <section>
        <Header/>
        <CreditPage/>
        <Footer/>
    </section>
</template>

<script>
    import Header from '@/components/views/header/Header'
    import CreditPage from '@/components/views/site-page/credit-main/Credit-page'
    import Footer from "@/components/views/footer/Footer";

    export default {
        name: "MainPage",
        components : {
            Header, CreditPage, Footer
        }
    }
</script>

<style scoped>

</style>