<script>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  components: {
    TheHeader,
    TheFooter,
  },
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
      ]
    }
  },
  methods: {
    getImagePath: function (img) {
      return new URL(`./assets/${img}`, import.meta.url).href;
    }
  }
}
</script>

<template>
  <TheHeader />

  <main>

    <div class="main-content">
      <div class="container">
        <h1> --Contente goes here--</h1>
      </div>

    </div>
    <div class="main-banner">
      <div class="container">
        <nav>
          <ul>
            <li v-for="link in navLinksMain">
              <img :src="getImagePath(link.src)" :alt="link.alt">
              <a href="#">{{ link.name }}</a>
            </li>

          </ul>
        </nav>
      </div>
    </div>


  </main>

  <TheFooter />
</template>

<style lang="scss">
@use "./styles/general.scss";
@use "./styles/partials/variables" as *;
@use "./styles/partials/mixins";

.main-content {
  color: white;
  height: 200px;
  @include mixins.d-flex-center;
}

.main-banner {
  height: 200px;
  background-color: $color-secondary;
}
</style>
