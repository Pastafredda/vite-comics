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
                    image: "../assets/img/buy-comics-subscriptions.png"
                },

                {
                    text: "COMIC SHOP LOCATOR",
                    url: "#",
                    image: "../assets/img/buy-comics-shop-locator.png"
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
                <a href="#" class="card" v-for="link in links">
                    <div class="logo-card">
                        <img :src="getImageUrl(link.image)" alt="">
                    </div>
                    <span href="#">{{ link.text }}</span>
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/mixins.scss' as *;

.jumbo {
    height: 140px;
    width: 100%;
    background-color: #232323;
    color: white;
}

.main-menu {

    background-color: #0080f8;
    height: 180px;
    display: flex;
    align-items: center;

    .card-menu {
        @include display-flex;

    }

    .card {
        display: flex;
        align-items: center;
    }

    .logo-card {
        height: 54px;
        width: 54px;
        padding-right: 10px;

    }

    span {
        font-size: 14px;
        color: white;
    }
}
</style>