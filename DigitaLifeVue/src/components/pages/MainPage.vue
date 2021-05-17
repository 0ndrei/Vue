<template>
    <section>
        <Header/>
        <HomePage/>
        <Footer/>
    </section>
</template>

<script>
import Header from '@/components/views/header/Header'
import HomePage from '@/components/views/site-page/home-main/Home-page'
import Footer from "@/components/views/footer/Footer";

export default {
    name: "MainPage",
    components: {
        Header,
        HomePage,
        Footer
    }
}
</script>

<style scoped>

</style>