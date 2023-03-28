<script>
export default {
    name: "TheHeader",
    data() {
        return {
            navLinks: [
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
                    href: '#characters',
                    name: 'Characters'
                },
                {
                    href: '#collectibles',
                    name: 'Collectibles'
                },
                {
                    href: '#videos',
                    name: 'Videos'
                },
                {
                    href: '#fans',
                    name: 'Fans'
                },
                {
                    href: '#news',
                    name: 'News'
                },
                {
                    href: '#shop',
                    name: 'Shop'
                }]
        }
    },
}
</script>

<template>
    <header>
        <div class="container ms_container">
            <div>
                <img src="../assets/img/dc-logo.png" alt="DC Logo">
            </div>
            <div class="h-100 my-5">
                <ul class="h-100">
                    <li class="h-100" v-for="(link, index) in navLinks" :key="index">
                        <a :href="link.href">{{ link.name }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";

ul {
    list-style: none;

    @include mixins.d-flex-center;

    & li {

        &:hover {
            border-bottom: 3px solid $color-secondary;
        }


        & a {
            color: $color-bg-footer;
            padding: 90px 15px;
            text-decoration: none;
            display: inline-block;

            &:hover {
                color: $color-secondary;
            }
        }
    }


}

.ms_container {

    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 200px
}
</style>
