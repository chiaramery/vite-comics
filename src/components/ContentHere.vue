<script>
import ItemCard from './ItemCard.vue';

export default {
    name: "ContentHere",
    data() {
        return {
            merch: [
                {
                    img: "buy-comics-digital-comics.png",
                    name: "DIGITAL COMICS",
                    href: "/digital_comics",
                },
                {
                    img: "buy-comics-merchandise.png",
                    name: "DC MERCHANDISE",
                    href: "/dc_merchandise",
                },
                {
                    img: "buy-comics-subscriptions.png",
                    name: "SUBSCRIPTION",
                    href: "/subscription",
                },
                {
                    img: "buy-comics-shop-locator.png",
                    name: "COMIC SHOP LOCATOR",
                    href: "/comic_shop_locator",
                },
                {
                    img: "buy-dc-power-visa.svg",
                    name: "DC POWER VISA",
                    href: "/dc_power_visa",
                },
            ],
            items: [
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel"
                }
            ],
        };
    },
    methods: {
        getImageUrl(url) {
            return new URL(url, import.meta.url).href;
        }
    },
    components: { ItemCard }
}
</script>

<template>
    <main>
        <div class="content-top">
            <div class="jumbotron">
                <button class="current">CURRENT SERIES</button>
            </div>

            <div class="wrapper-item">
                <div class="container">
                    <div class="row">
                        <ItemCard v-for="(item, index) in items" :key="index" :title="item.series.toLocaleUpperCase()"
                            :imgUrl="item.thumb" :type="item.type" />
                    </div>
                    <button class="load">LOAD MORE</button>
                </div>
            </div>
            <div class="container">
                <h1>{{ title }}</h1>

            </div>
        </div>
        <div class="content-nav">
            <ul class="wrap-card">
                <div class="container">
                    <li class="card" v-for="(icon, index) in merch" :key="index">
                        <img :src="getImageUrl(`../assets/img/${icon.img}`)" :alt="icon.href">
                        <a :href="icon.href"> {{ icon.name }}</a>

                    </li>
                </div>
            </ul>

        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/frame/mixins.scss" as *;
@use "../styles/general.scss" as *;

main {
    width: 100%;

    .content-top {
        margin-top: 6rem;
        position: relative;

        .jumbotron {
            margin-top: 6rem;
            height: 16rem;
            background-image: url(../assets/img/jumbotron.jpg);
            background-size: cover;

            .current {
                background-color: rgb(29 134 247);
                border-color: rgb(29 134 247);
                color: white;
                padding: .5em;
                cursor: pointer;
                position: absolute;
                top: 16rem;
                left: 18rem;
                transform: translate(-50%, -50%);
            }
        }

        .wrapper-item {
            background-color: rgb(28 28 28);
            padding: 3em;

            .container {

                .row {
                    display: flex;
                    justify-content: center;
                    flex-wrap: wrap;
                    gap: .5em;
                }

                .load {
                    background-color: rgb(29 134 247);
                    border-color: rgb(29 134 247);
                    color: white;
                    padding: .5em;
                    cursor: pointer;
                    position: absolute;
                    left: 50%;
                    top: 97%;
                    transform: translate(-50%, -50%);
                }
            }
        }

        h1 {
            text-align: center;
            line-height: 6rem;
            color: white;
        }
    }

    .content-nav {
        height: 8rem;
        background-color: rgb(29 134 247);
        display: flex;
        align-items: center;

        .wrap-card {
            @include flex("center");
            list-style: none;
            width: 100%;

            .card {
                padding: 3em;
                width: 100%;
                @include flex("altro");

                img {
                    width: 30px;
                }

                a {
                    font-size: .8em;
                    color: white;
                }
            }
        }
    }
}
</style>