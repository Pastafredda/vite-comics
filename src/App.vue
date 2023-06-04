<script>
import Header from './components/header.vue'
import HomeMenu from './components/HomeMenu.vue'
import Footer from './components/Footer.vue'
import Jumbo from './components/Jumbo.vue'



export default {
    components: {
        Header,
        Jumbo,
        HomeMenu,
        Footer
    }
}

</script>

<template>
    <Header />
    <Jumbo />
    <HomeMenu />
    <Footer />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/mixins.scss' as *;
</style>
