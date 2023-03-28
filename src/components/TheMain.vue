<script>
import TheCards from './TheCards.vue';
export default {
    components: {
        TheCards,
    },
    name: "TheMain",
    data() {
        return {
            imagePath: 'buy-comics-digital-comics.png',
            navLinksMain: [
                {
                    src: 'buy-comics-digital-comics.png',
                    alt: 'BuyDigitalComics',
                    name: 'DIGITAL COMICS'
                },
                {
                    src: 'buy-comics-merchandise.png',
                    alt: 'BuyMerchandise',
                    name: 'DC MERCHANDISE'
                },
                {
                    src: 'buy-comics-subscriptions.png',
                    alt: 'BuySubscriptions',
                    name: 'SUBSCRIPTION'
                },
                {
                    src: 'buy-comics-shop-locator.png',
                    alt: 'BuyShopLocator',
                    name: 'COMIC SHOP LOCATOR'
                },
                {
                    src: 'buy-dc-power-visa.svg',
                    alt: 'BuyPowerVisa',
                    name: 'DC POWER VISA'
                },
            ],
            cardComicArray: [
                {
                    "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <main>

        <div class="main-content">
            <div class="container">
                <TheCards :cardsarray="cardComicArray" />
            </div>

        </div>
        <div class="main-banner">
            <div class="container h-100">
                <nav class="h-100">
                    <ul class="d-flex h-100 justify-content-around  ">
                        <li class="h-100 d-flex align-items-center p-2" v-for="(link, index) in navLinksMain" :key="index">
                            <img :src="getImagePath(link.src)" :alt="link.alt">
                            <a class="px-2" href="#">{{ link.name }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>


    </main>
</template>
<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";
@use "../styles/general.scss";

.main-content {
    color: white;
    @include mixins.d-flex-center;
}

.main-banner {
    height: 200px;
    background-color: $color-secondary;

    & a {
        color: $color-primary;
    }

    & img {
        height: 60px;
    }

}


li {

    &:last-child img {
        height: 40px;
    }
}
</style>