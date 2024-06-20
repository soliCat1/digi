<template>
  <li>
    <label>
      <input class="visually-hidden" type="checkbox">
      <div>
        <SvgSprite :name="'tick'"></SvgSprite>
      </div>
      <p>{{ attribute.attr }}</p>
      <span>{{ attribute.count }}</span>
    </label>
  </li>
</template>

<script>
import SvgSprite from '@/components/ui/SvgSprite.vue';

export default {
  props: {
    attribute: {
      type: Object,
      required: true
    }
  },
  components: { SvgSprite }
}
</script>

<style lang="scss" scoped>
label {
  display: flex;
  align-items: center;
  cursor: pointer;
}

div {
  width: 20px;
  height: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid $color-border;
  border-radius: 4px;
  margin-right: 12px;
}

p {
  margin-right: auto;
}

label:hover > div {
  border-color: $color-brand;
}

input:checked + div {
  background-color: $color-brand;
  border-color: $color-brand;
}

span {
  font-size: 12px;
  line-height: 14px;
  color: $color-font-second;
  padding-right: 12px;
}
</style>