<template>
  <header class="header">
    <a href="/" class="header__logo">
      <SvgSprite :name="'logo'"></SvgSprite>
    </a>
    <ButtonComponent class="catalog">Каталог</ButtonComponent>
    <HeaderSearch></HeaderSearch>
    <nav class="header__nav">
      <ul>
        <li>
          <a href="/">Информация о компании</a>
        </li>
        <li>
          <a href="/">Контакты</a>
        </li>
        <li>
          <a href="/">Полезные ссылки</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import SvgSprite from '@/components/ui/SvgSprite.vue';
import ButtonComponent from '@/components/ui/ButtonComponent.vue';
import HeaderSearch from '@/components/ui/HeaderSearch.vue';

export default {
  components: { SvgSprite, ButtonComponent, HeaderSearch }
}

</script>

<style lang="scss">
.header {
  padding: 8px 16px;
  min-width: 375px;

  @media (min-width: $desktop-width) {
    padding: 12px 128px;
    display: flex;
  }

  @media (min-width: $big-desktop-width) {
    padding: 12px 100px;
    max-width: 1920px;
    margin: 0 auto;
  }
}

.header__logo {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
    margin-right: 8px;
  }
}

.header__nav {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
    display: flex;
    gap: 20px;
    align-items: center;
  }
}

.header__nav ul {
  display: flex;
  gap: 20px;
  align-items: center;
  list-style: none;
}

.header__nav a {
  display: block;
  font-family: "Inter", sans-serif;
  color: #393939;
  font-weight: 400;
  font-size: 14px;
  line-height: 14px;
  text-decoration: none;

  &:hover {
    color: $color-font-hover;
  }
}
</style>