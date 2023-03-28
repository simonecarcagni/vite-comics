<script>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';
import TheMain from './components/TheMain.vue';

export default {
  components: {
    TheMain,
    TheHeader,
    TheFooter,
  },
} 
</script>

<template>
  <TheHeader />

  <TheMain />

  <TheFooter />
</template>

<style lang="scss">
@use "./styles/general.scss";
@use "./styles/partials/variables" as *;
@use "./styles/partials/mixins";
</style>
