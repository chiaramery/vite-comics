<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    title: "CHARACTERS",
                    href: "/characters",
                    active: false,
                },
                {
                    title: "COMICS",
                    href: "/comics",
                    active: true,
                },
                {
                    title: "MOVIES",
                    href: "/movies",
                    active: false,
                },
                {
                    title: "TV",
                    href: "/tv",
                    active: false,
                },
                {
                    title: "GAMES",
                    href: "/games",
                    active: false,
                },
                {
                    title: "COLLECTIBLES",
                    href: "/collectibles",
                    active: false,
                },
                {
                    title: "VIDEOS",
                    href: "/videos",
                    active: false,
                },
                {
                    title: "FANS",
                    href: "/fans",
                    active: false,
                },
                {
                    title: "NEWS",
                    href: "/news",
                    active: false,
                },
                {
                    title: "SHOP",
                    href: "/shop",
                    active: false,
                },

            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <!-- LOGO -->
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
                <!-- NAV -->
            </div>
            <nav class="header-nav">
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class="{ 'active': link.active }" :href="link.href">{{ link.title}}</a>
                    </li>
                </ul>
            </nav>

        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/frame/mixins.scss" as *;

header {
    position: fixed;
    z-index: 999;
    top: 0;
    width: 100%;
    height: 6rem;
    background-color: rgb(255 255 255);
    @include flex ("altro");

    .container {
        list-style: none;
        display: flex;
        justify-content: space-around;

        .logo {
            display: flex;
            align-items: center;

            img {
                width: 50px;
                line-height: 6rem;
            }
        }

        .header-nav {

            ul {
                @include flex("altro");
                list-style: none;


                li {
                    margin: 0px .8rem;


                    a {
                        font-size: .8em;
                        color: black;
                        cursor: pointer;
                        display: inline-block;
                        line-height: 6rem;
                        border-bottom: 3px solid transparent;

                        &:hover,
                        &.active {
                            border-bottom: 3px solid rgb(29 134 247);
                            color: rgb(29 134 247);
                        }
                    }
                }
            }
        }
    }



}
</style>