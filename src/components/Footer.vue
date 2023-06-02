<script>
export default {
    name: "Footer",
    data() {
        return {
            links: [
                {
                    title: 'DC COMICS',
                    texts: [
                        {
                            text: 'Characters'
                        },

                        {
                            text: 'Comics'
                        },
                        {
                            text: 'Movies'

                        },
                        {
                            text: 'TV'

                        },
                        {
                            text: 'Games'

                        },
                    ]
                },
                {
                    title: 'SHOP',
                    texts: [
                        {
                            text: 'Shop DC'
                        },

                        {
                            text: 'Shop DC Collectibles'
                        },
                    ]
                },

                {
                    title: 'DC',
                    texts: [
                        {
                            text: 'Terms Of Use'
                        },

                        {
                            text: 'Privacy policy (New)'
                        },

                        {
                            text: 'Ad Choices'
                        },

                        {
                            text: 'Advertising'
                        },

                        {
                            text: 'Jobs'
                        },

                        {
                            text: 'Subscriptions'
                        },

                        {
                            text: 'Talent Workshops'
                        },

                        {
                            text: 'CPSC Certificates'
                        },

                        {
                            text: 'Rating'
                        },

                        {
                            text: 'Shop Help'
                        },

                        {
                            text: 'Contact Us'
                        },
                    ]
                },
                {
                    title: 'SITES',
                    texts: [
                        {
                            text: 'DC'
                        },

                        {
                            text: 'MAD Magazine'
                        },

                        {
                            text: 'DC Kids'
                        },

                        {
                            text: 'DC Universe'
                        },

                        {
                            text: 'DC Power Visa'
                        }
                    ]
                }

            ]
        }
    }
}

</script>

<template>
    <footer>
        <div class="container">
            <div class="container-footer">
                <div class="menu-footer">
                    <div class="card" v-for="(link, index) in links">
                        <h5>{{ link.title }}</h5>
                        <ul>
                            <li v-for="(text, index) in link.texts">
                                <a href="#">{{ text.text }}</a>
                            </li>
                        </ul>
                    </div>

                </div>
                <div class="logo-footer">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>

    </footer>
</template>

<style scoped lang="scss">
@use '../styles/mixins.scss' as *;

footer {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 300px;

    .container-footer {
        display: flex;
        justify-content: space-between;

        .menu-footer {
            display: flex;
            gap: 15px;
            padding: 30px;


            h5 {
                color: white;

            }

            a {
                color: #777570;
                font-size: 12px;
            }
        }

        .logo-footer {
            height: 400px;
        }
    }


}
</style>