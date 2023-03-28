<script>
export default {
    name: "TheFooter",
    data() {
        return {
            iconsArray: [
                {
                    href: '#facebook',
                    fa_icon: 'facebook-f'
                },
                {
                    href: '#twitter',
                    fa_icon: 'twitter'
                },
                {
                    href: '#youtube',
                    fa_icon: 'youtube'
                },
                {
                    href: '#pinterest',
                    fa_icon: 'pinterest-p'
                },
                {
                    href: '#location',
                    fa_icon: 'location-pin'
                },
            ],
            linksDcComic: [
                {
                    href: '#characters',
                    name: 'Characters'
                },
                {
                    href: '#comics',
                    name: 'Comics'
                },
                {
                    href: '#movies',
                    name: 'Movies'
                },
                {
                    href: '#tv',
                    name: 'TV'
                },
                {
                    href: '#games',
                    name: 'Games'
                },
                {
                    href: '#videos',
                    name: 'Videos'
                },
                {
                    href: '#news',
                    name: 'News'
                },
            ],

            linksShop: [
                {
                    href: '#shopDc',
                    name: 'Shop DC'
                },
                {
                    href: '#shopDcCollectibles',
                    name: 'Shop DC Collectibles'
                },

            ],
            linksDc: [
                {
                    href: '#facebook',
                    name: 'Terms Of Use'
                },
                {
                    href: '#twitter',
                    name: 'Privacy policy(New)'
                },
                {
                    href: '#youtube',
                    name: 'Ad Choices'
                },
                {
                    href: '#pinterest',
                    name: 'Advertising'
                },
                {
                    href: '#location',
                    name: 'Jobs'
                },
                {
                    href: '#facebook',
                    name: 'Subscriptions'
                },
                {
                    href: '#twitter',
                    name: 'Talent Workshops'
                },
                {
                    href: '#youtube',
                    name: 'CPSC Certificates'
                },
                {
                    href: '#pinterest',
                    name: 'Ratings'
                },
                {
                    href: '#location',
                    name: 'Shop Help'
                },
                {
                    href: '#location',
                    name: 'Contact Us'
                },
            ],
            linksSite: [
                {
                    href: '#facebook',
                    name: 'DC'
                },
                {
                    href: '#twitter',
                    name: 'MAD Magazine'
                },
                {
                    href: '#youtube',
                    name: 'DC Kids'
                },
                {
                    href: '#pinterest',
                    name: 'DC Universe'
                },
                {
                    href: '#location',
                    name: 'DC Power Visa'
                },
            ],
        }
    },

}

</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container h-100 d-flex">

                <div class="col-1 h-100 mt-5">
                    <h5>DC COMICS</h5>
                    <ul>
                        <li v-for="(link, index) in linksDcComic" :key="index">
                            <a :href="link.href">{{ link.name }}</a>
                        </li>
                    </ul>
                    <h5>SHOP</h5>
                    <ul>
                        <li v-for="(link, index) in linksShop" :key="index">
                            <a :href="link.href">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-1 h-100 mt-5">
                    <h5>DC</h5>
                    <ul>
                        <li v-for="(link, index) in linksDc" :key="index">
                            <a href="">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
                <div class=" col-1 h-100 mt-5">
                    <h5>SITES</h5>
                    <ul>
                        <li v-for="(link, index) in linksSite" :key="index">
                            <a href="">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container ms_space_between">
                <div class="button-container">
                    <button> SIGN-UP NOW!</button>
                </div>
                <div class="followus-container mt-3 d-flex align-items-center">
                    <h5 class="mb-3">FOLLOW US</h5>
                    <ul>
                        <li class="d-block" v-for="icon in iconsArray">
                            <a class="icon-container" :href="icon.href">
                                <i class="fab" :class="'fa-' + icon.fa_icon"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";

.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    height: 400px;

    & h5 {
        color: white;

    }

    & a {
        color: #797979;
        font-size: 14px;
    }

    & .col-1 {
        width: 150px;
    }
}

.footer-bottom {
    height: 100px;
    background-color: $color-bg-footer;
}

.ms_space_between {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.followus-container {
    @include mixins.d-flex-center;

    & * {
        padding: 0px 10px;

    }

    & ul {
        display: flex;
        align-items: center;
    }
}

h5 {
    color: $color-secondary;
}

.icon-container {
    height: 50px;
    width: 50px;
    display: inline-block;
    background-color: #797979;
    border-radius: 50%;
    @include mixins.d-flex-center;
    text-decoration: none;

    & i {
        font-size: 18px;
        color: $color-bg-footer;
    }

}

button {
    border: 2px solid $color-secondary;
    padding: 10px;
    background-color: $color-bg-footer;
    color: $color-primary;
}
</style>
