<template>
    <header class="bg-white">
        <div class="container d-flex justify-content-between mt-3 mb-3  ">
            <img src="/img/dc-logo.png" alt="Logo DC comics">
            <ul class="d-flex align-items-center list-unstyled gap-3">
                <li v-for="(item, index) in menu" :key="index">
                    <a class="text-decoration-none text-uppercase" :href="item.url">{{ item.title }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            menu: [
                {
                    title: "characters",
                    url: "#"
                },
                {
                    title: "comics",
                    url: "#"
                },
                {
                    title: "movies",
                    url: "#"
                },
                {
                    title: "tv",
                    url: "#"
                },
                {
                    title: "games",
                    url: "#"
                },
                {
                    title: "collectibles",
                    url: "#"
                },
                {
                    title: "videos",
                    url: "#"
                },
                {
                    title: "fans",
                    url: "#"
                },
                {
                    title: "news",
                    url: "#"
                },
                {
                    title: "shop",
                    url: "#"
                },
            ],
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

a {
    color: gray;

    &:hover {
        color: $azure;
    }

}
</style>