<script>
export default {
    name: "TheCards",
    data() {
        return {}
    },
    props: ['cardsarray'],
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}

</script>


<template>
    <div class="container my-5">
        <ul class="d-flex flex-wrap g-5">
            <li class="card-container mx-4 " v-for="(element, index) in cardsarray" :key="index">
                <div class="ms_card">
                    <img class="comic-card" :src="element.thumb" alt="">
                </div>
                <h6 class="p-1">{{ element.series }} - {{ element.price }}</h6>
            </li>
        </ul>
    </div>
    <div class="load-more">
        <button>LOAD MORE</button>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";
@use "../styles/general.scss";


.ms_card {
    height: 200px;
    width: 200px;
    overflow-y: hidden;

    & img {
        transform: translate(0px, -10px);
        width: 100%;
    }
}

.card-container {
    width: calc(100% / 6 - 3rem);
}

.load-more {
    width: 132px;
    margin: 20px auto;

    & button {
        background-color: $color-secondary;
        border-color: $color-secondary;
        color: white;
        font-size: 12px;
        padding: 10px 24px;
    }
}
</style>