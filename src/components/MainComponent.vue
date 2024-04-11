<template>
    <main>
        <div class="cards">
            <div class="container">
                <h1>Content goes here</h1>
            </div>
        </div>
        <div class="sub-nav">
            <div class="container d-flex align-items-center justify-content-center ">
                <ul class="d-flex list-unstyled justify-content-center align-items-center gap-5 ">
                    <li class="d-flex gap-3 align-items-center" v-for="item in items" :key="item.imageUrl">
                        <img :src="'/img/'+ item.image" alt="Image description">
                        <span class="text-uppercase text-white ">{{ item.text }}</span>
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'MainComponent',
    data() {
        return {
            items: [
                { image: "buy-comics-digital-comics.png", text: "digital comics" },
                { image: "buy-comics-merchandise.png", text: "dc merchandise" },
                { image: "buy-comics-shop-locator.png", text: "comic shop locator" },
                { image: "buy-comics-subscriptions.png", text: "subscription" },
                { image: "buy-dc-power-visa.svg", text: "dc power visa"}
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.cards {
    background-color: $darkGray;
    display: inline-block;
    width: 100%;
}

img {
    width: 60px;
}

.container {
    height: 150px;
}

.sub-nav {
    background-color: $azure;
    display: inline-block;
    width: 100%;
}
</style>