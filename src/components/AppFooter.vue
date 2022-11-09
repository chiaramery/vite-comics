<script>
export default {
    name: "AppFooter",
    data() {
        return {
            dcComics: [
                {
                    title: "DC COMICS",
                    links: [
                        "Characters",
                        "Comics",
                        "Movies",
                        "TV",
                        "Games",
                        "Videos",
                        "News",
                    ],
                },
                {
                    title: "SHOP",
                    links: [
                        "Shop DC",
                        "Shop DC Collectibles",
                    ],
                },
                {
                    title: "DC",
                    links: [
                        "Terms Of Use",
                        "Privacy Policy(New)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshops",
                        "CPSC Certificates",
                        "Rantings",
                        "Shop Help",
                        "Contact Us",
                    ],
                },
                {
                    title: "SITES",
                    links: [
                        "DC",
                        "MAD",
                        "DC Kids",
                        "DC Universe",
                        "DC Power Visa",
                    ],
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <ul>
                    <li v-for="(title, index) in dcComics" :key="index">
                        <h5>{{ title.title }}</h5>
                        <p>Lorem ipsum dolor</p>
                        <p>Lorem ipsum dolor</p>
                        <p>Lorem ipsum dolor</p>
                        <p>Lorem ipsum dolor</p>
                        <p>Lorem ipsum dolor</p>

                    </li>
                </ul>
            </div>
            <div class="footer-bottom">
                <div class="container">
                    <div class="left">
                        <button>SIGN-UP NOW!</button>
                    </div>
                    <div class="right">
                        <h1>FOLLOW US</h1>
                        <div class="icon">
                            <img src="../assets/img/footer-facebook.png" alt="">
                            <img src="../assets/img/footer-twitter.png" alt="">
                            <img src="../assets/img/footer-youtube.png" alt="">
                            <img src="../assets/img/footer-pinterest.png" alt="">
                            <img src="../assets/img/footer-periscope.png" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/frame/mixins.scss" as *;

footer {
    width: 100%;

    .footer-top {
        width: 100%;
        background-image: url("../assets/img/footer-bg.jpg");

        ul {
            list-style: none;

            li {
                color: white;

                p {
                    color: gray;
                    font-size: .7em;
                    padding: .5em;
                }
            }
        }
    }

    .footer-bottom {
        width: 100%;
        padding: 1em;
        @include flex ("altro");
        background-color: rgb(48 48 48);

        .container {
            justify-content: space-between;

            .left {
                display: flex;
                align-items: center;

                button {
                    cursor: pointer;
                    color: white;
                    padding: .5em;
                    background-color: rgb(48 48 48);
                    border: 2px solid rgb(29 134 247);
                }
            }

            .right {
                @include flex ("altro");

                h1 {
                    color: rgb(29 134 247);
                    font-size: 1em;
                    cursor: pointer;
                    margin-right: .5em;
                }

                .icon img {
                    margin: .3em;
                }

            }

        }
    }
}
</style>