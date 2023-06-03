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
                <div class="logo-footer"></div>
            </div>
        </div>
        <div class="finale">
            <div class="container">
                <div class="nav-footer">
                    <div class="sign-up">
                        <a href="#">SIGN-UP NOW!</a>
                    </div>
                    <div>
                        <ul class="social">
                            <li>FOLLOW US</li>
                            <li><a href="#"><img src="../assets/img/footer-facebook.png" alt=""></a></li>
                            <li><a href="#"><img src="../assets/img/footer-twitter.png" alt=""></a></li>
                            <li><a href="#"><img src="../assets/img/footer-youtube.png" alt=""></a></li>
                            <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt=""></a></li>
                            <li><a href="#"><img src="../assets/img/footer-periscope.png" alt=""></a></li>
                        </ul>
                    </div>
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
    position: relative;

    .container-footer {
        display: flex;
        justify-content: space-between;

        .menu-footer {
            display: flex;
            gap: 20px;
            padding: 30px;


            h5 {
                color: white;
                margin-bottom: 10px;

            }

            a {
                color: #777570;
                font-size: 10px;
            }
        }

        .logo-footer {
            background-image: url(../assets/img/dc-logo-bg.png);
            height: 300px;
            width: 460px;
            background-repeat: no-repeat;
            background-size: 100%;
            background-position: 0 -75px;
        }
    }

}

.finale {
    background-color: #313232;
    width: 100%;
    height: 100px;
    display: flex;
    align-items: center;

    .nav-footer {
        @include display-flex;

        .sign-up {


            a {
                padding: 10px;
                color: white;
                text-align: center;
                border: 2px solid #007be9;
                font-size: 14px;

            }
        }

        .social {
            display: flex;
            align-items: center;

            li {
                font-size: 16px;
                color: #0080f8;
                font-weight: 600;
                margin-right: 20px;

                img {
                    width: 24px;
                }

            }
        }
    }


}
</style>