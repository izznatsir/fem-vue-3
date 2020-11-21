<template>
    <div class="unit" v-for="unit in manifest" :key="unit.item">
        <ProductCard :item="unit.item" :url="unit.url"></ProductCard>
    </div>
</template>

<script>
import ProductCard from "./components/ProductCard.vue";

export default {
    name: "App",
    components: {
        ProductCard,
    },
    data() {
        return {
            manifest: [
                {
                    item: "backpack",
                    url:
                        "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/backpack.jpg",
                },
                {
                    item: "tshirt",
                    url:
                        "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/tshirt.jpg",
                },
                {
                    item: "sweatshirt",
                    url:
                        "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/sweatshirt.jpg",
                },
            ],
        };
    },
};
</script>

<style lang='scss'>
body,
html {
    font-family: "PT Serif", serif;
}

#app {
    display: flex;
    justify-content: center;
}

.special {
    font-family: "Montserrat", sans-serif;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-size: 12px;
}

h1,
h2,
h3,
li {
    @extend .special;
}

h2 {
    font-size: 20px;
    margin: 0 0 5px;
    text-align: center;
}

li {
    list-style: none;
    display: inline-block;
}

input {
    background: #eee;
}
</style>
