<template>
  <div>
    <SvgSprite :name="'filters-search'"></SvgSprite>
    <input type="text" placeholder="Поиск" v-model="searchValue">
    <button class="reset" type="button" @click="clearValue">
      <SvgSprite :name="'search-reset'"></SvgSprite>
    </button>
  </div>
</template>

<script>
import SvgSprite from '@/components/ui/SvgSprite.vue';

export default {
  components: { SvgSprite },
  data: () => ({
    searchValue: ''
  }),
  methods: {
    clearValue() {
      this.searchValue = ''
    }
  }
}  
</script>

<style lang="scss" scoped>
div {
  position: relative;
}

div>svg {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  left: 16px;
}

input {
  background-color: transparent;
  font-family: inherit;
  font-size: 16px;
  line-height: 150%;
  border: 1px solid $color-font-second;
  border-radius: 10px;
  padding: 10px 50px 10px 40px;

  &:focus {
    outline: none;
    border-color: $color-brand;
  }
}

.reset {
  border: none;
  font-family: inherit;
  padding: 0;
  cursor: pointer;
  background-color: transparent;
  transition: all 0.2s ease;
  opacity: 0.3;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 12px;

  &:hover {
    opacity: 1;
  }
}

input:placeholder-shown+.reset {
  display: none;
}
</style>