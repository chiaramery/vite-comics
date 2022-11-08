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
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/frame/mixins.scss" as *;

header {
    width: 100%;
    height: 8rem;
    background-color: lightgray;
    @include flex ("altro");

    .header-nav {
        @include flex ("center");

        ul {
            @include flex("center");
            list-style: none;

            li {
                margin: 0px .8rem;

                a {
                    color: black;

                    &:hover,
                    &.active {
                        color: blue;
                    }
                }
            }
        }
    }


}
</style>