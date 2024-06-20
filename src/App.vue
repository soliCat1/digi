<template>
  <div id="app">
    <HeaderComponent></HeaderComponent>
    <div class="container">
      <FiltersComponent></FiltersComponent>
      <CardsList></CardsList>
    </div>
  </div>
</template>

<script>
import HeaderComponent from '@/components/blocks/HeaderComponent.vue';
import CardsList from './components/blocks/CardsList.vue';
import FiltersComponent from '@/components/blocks/FiltersComponent.vue';

export default {
  name: "App",
  components: { HeaderComponent, CardsList, FiltersComponent }
}
</script>

<style lang="scss">
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  white-space: nowrap;
  border: 0;
  clip: rect(0 0 0 0);
  clip-path: inset(100%);
}

#app {
  font-family: "PT Sans", sans-serif;
  font-size: 14px;
  line-height: 16px;
  font-weight: 400;
  font-style: normal;
  color: $color-font-main;
}

.container {
  padding: 0 16px;
  min-width: 375px;

  @media (min-width: $desktop-width) {
    padding: 0 100px;
    display: grid;
    grid-template-columns: 280px auto;
    gap: 36px;
    max-width: 1920px;
    margin: 0 auto;
  }
}
</style>
