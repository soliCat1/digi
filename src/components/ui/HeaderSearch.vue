<template>
  <form @reset="isActive = false">
    <SvgSprite :name="svgName"></SvgSprite>
    <input type="text" :placeholder="placeholder">
    <div class="border"></div>
    <ButtonComponent type="reset" class="reset">
      <SvgSprite :name="'search-reset'"></SvgSprite>
    </ButtonComponent>
    <ButtonComponent type="submit" class="submit">Найти</ButtonComponent>
  </form>
</template>

<script>
import SvgSprite from '@/components/ui/SvgSprite.vue';
import ButtonComponent from '@/components/ui/ButtonComponent.vue';

export default {
  components: { SvgSprite, ButtonComponent },
  computed: {
    svgName() {
      if (window.matchMedia("(min-width: 1440px)").matches) {
        return 'search'
      } else {
        return 'search-arrow'
      }
    },
    placeholder() {
      if (window.matchMedia("(min-width: 1440px)").matches) {
        return 'Поиск по 100 000 товаров'
      } else {
        return ''
      }
    }
  }
}  
</script>

<style lang="scss" scoped>
form {
  display: flex;
  align-items: center;
  gap: 16px;
  position: relative;

  @media (min-width: $desktop-width) {
    flex-grow: 1;
    margin-right: 24px;
  }
}

form>svg {
  @media (min-width: $desktop-width) {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    left: 16px;
  }
}

.border {
  position: absolute;
  bottom: -8px;
  left: 36px;
  right: 0;
  height: 1px;
  background-color: $color-border;

  @media (min-width: $desktop-width) {
    display: none;
  }
}

input {
  background-color: transparent;
  border: none;
  font-family: inherit;
  font-size: 16px;
  line-height: 150%;
  flex-grow: 1;

  &:focus {
    outline: none;

    &+.border {
      background-color: $color-brand;
    }
  }

  @media (min-width: $desktop-width) {
    padding: 11px 127px 11px 48px;
    border: 1px solid $color-font-second;
    border-radius: 10px;

    &:focus {
      border-color: $color-brand;
    }
  }
}

input:placeholder-shown~.reset {
  display: none;
}

input:placeholder-shown~.submit {
  @media (min-width: $desktop-width) {
    display: none;
  }
}
</style>