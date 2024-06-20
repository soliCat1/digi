<template>
  <div v-if="isActive">
    Хит продаж
    <SvgSprite :name="'hit'"></SvgSprite>
  </div>
</template>

<script>
import SvgSprite from '@/components/ui/SvgSprite.vue';

export default {
  props: {
    isActive: {
      type: Boolean,
      required: true
    }
  },
  components: { SvgSprite }
}
</script>

<style lang="scss" scoped>
div {
  background-color: $color-white;
  position: absolute;
  top: 12px;
  left: 12px;
  display: flex;
  align-items: center;
  padding: 6px 8px;
  border-radius: 5px;
  border: 1px solid $scroll-bar;
  gap: 4px;
}
</style>