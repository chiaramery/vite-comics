<script>
export default {
    name: "ContentHere",
    data() {
        return {
            title: '--> Content goes here <--',
            merch: [
                {
                    image: "buy-comics-digital-comics.png",
                    name: 'DIGITAL COMICS',
                    href: "/digital_comics",
                },
                {
                    image: "buy-comics-merchandise.png",
                    name: 'DC MERCHANDISE',
                    href: "/dc_merchandise",
                },
                {
                    image: "buy-comics-subscriptions.png",
                    name: 'SUBSCRIPTION',
                    href: "/subscription",
                },
                {
                    image: "buy-comics-shop-locator.png",
                    name: 'COMIC SHOP LOCATOR',
                    href: "/comic_shop_locator",
                },
                {
                    image: "buy-dc-power-visa.svg",
                    name: 'DC POWER VISA',
                    href: "/dc_power_visa",
                },
            ]
        }
    }
}
</script>

<template>
    <main>
        <div class="content-top">
            <div class="container">
                <h1>{{ title }}</h1>

            </div>
        </div>
        <div class="content-nav">
            <ul>
                <li class="card" v-for="(element, index) in merch" :key="index">
                    <img src="../assets/img/buy-comics-digital-comics.png" :alt="element.href">
                    <a :href="element.href"> {{ element.name }}</a>
                </li>
            </ul>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/frame/mixins.scss" as *;

main {
    width: 100%;

    .content-top {
        height: 6rem;
        background-color: black;

        h1 {
            text-align: center;
            line-height: 6rem;
            color: white;
        }
    }

    .content-nav {
        background-color: blue;

        ul {
            @include flex("center");
            list-style: none;

            .card {
                padding: 3em 6em;
                width: calc(100% / 5);
                @include flex("altro");

                a {
                    margin-left: 1em;
                    font-size: .8em;
                    color: white;
                }
            }
        }
    }
}
</style>