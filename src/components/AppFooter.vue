<script>
export default {
    name: "AppFooter",
    data() {
        return {
            dcComics: [
                {
                    title: "DC COMICS",
                },
                {
                    title: "SHOP",
                },
                {
                    title: "DC",
                },
                {
                    title: "SITES",
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
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>

                    </li>
                </ul>
            </div>
            <div class="footer-bottom">
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
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/frame/mixins.scss" as *;

footer {
    width: 100%;
    height: 3em;

    .footer-top {
        width: 100%;
        background-image: url("../assets/img/footer-bg.jpg");

        ul {
            list-style: none;

            li {
                color: white;

                p {
                    font-size: .7em;
                    padding: .5em;
                }
            }
        }
    }

    .footer-bottom {
        width: 100%;
        @include flex ("altro");
        position: fixed;
        bottom: 0;
        background-color: darkgray;

        .left {
            button {
                cursor: pointer;
            }
        }

        .right {
            @include flex ("altro");

            h1 {
                color: blue;
                font-size: 1em;
                cursor: pointer;
            }

            .icon img {
                margin: .3em;
            }
        }
    }
}
</style>