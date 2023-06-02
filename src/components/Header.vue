<script>
export default {
    name: "Header",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },

                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },

                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },

                {
                    text: "TV",
                    url: "#",
                    current: false
                },

                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },

                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },

                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },

                {
                    text: "FANS",
                    url: "#",
                    current: false
                },

                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },

                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },

            ]
        }
    }

}
</script>

<template>
    <header>
        <div class="container">
            <div class="container-header">
                <div class="logo">
                    <a href="/">
                        <img src="../assets/img/dc-logo.png" alt="">
                    </a>
                </div>
                <div>
                    <ul class="nav-menu">
                        <li v-for="link in links"><a :href="link.url" :class="link.current ? 'active' : 'black'">{{
                            link.text }}</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/mixins.scss' as *;

.container-header {
    @include display-flex;
    padding: 20px;

    .logo {
        width: 64px;
    }

    .nav-menu {
        display: flex;
        gap: 16px;

        li {
            list-style-type: none;
            font-size: 12px;

        }

        a {
            font-weight: 500;
        }
    }
}
</style>