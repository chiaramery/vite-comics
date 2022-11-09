<script>
export default {
    name: "ItemCard",
    props: {
        imgUrl: String,
        title: String,
        type: String,
        price: String
    }
}
</script>

<template>
    <div class="item">
        <img :src="imgUrl" :alt="title">
        <h6>{{ title}}</h6>
    </div>
</template>

<style lang="scss" scoped>
.item {
    width: calc(100% / 7);

    h6 {
        font-size: .5em;
        margin-top: .5em;
        color: white;
    }

    img {
        background-size: cover;
        width: 100px;
    }
}
</style>