<script>
export default {
    name: "Main",
    data() {
        return {
            links: [
                {
                    text: "DIGITAL COMICS",
                    url: "#",
                    image: "../assets/img/buy-comics-digital-comics.png"
                },

                {
                    text: "DC MERCHANDISE",
                    url: "#",
                    image: "../assets/img/buy-comics-merchandise.png"
                },

                {
                    text: "SUBSCRIPTION",
                    url: "#",
                    image: "../assets/img/buy-comics-shop-locator.png"
                },

                {
                    text: "COMIC SHOP LOCATOR",
                    url: "#",
                    image: "../assets/img/buy-comics-subscriptions.png"
                },

                {
                    text: "DC POWER VISA",
                    url: "#",
                    image: "../assets/img/buy-dc-power-visa.svg"
                },
            ]
        }
    },
    methods: {
        getImageUrl: function (imgPath) {
            return new URL(imgPath, import.meta.url).href
        }
    }
}

</script>

<template>
    <div class="jumbo">
        <div class="container">
            Content goes here
        </div>
    </div>

    <div class="main-menu">
        <div class="container">
            <div class="card-menu">
                <div class="logo-card" v-for="link in links">
                    <img :src="getImageUrl(link.image)" alt="">
                    <span>{{ link.text }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.jumbo {
    height: 140px;
    width: 100%;
    background-color: #232323;
    color: white;
}

.main-menu {
    background-color: #0080f8;
    padding: 20px;
}

.logo-card {
    width: 40px;

}
</style>