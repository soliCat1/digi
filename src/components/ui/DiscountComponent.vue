<template>
  <div>{{ discount }}</div>
</template>

<script>
export default {
  props: {
    discount: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
div {
  color: $color-white;
  background-color: $color-brand;
  font-weight: 700;
  padding: 6px 10px;
  border-radius: 5px;
  position: absolute;
  bottom: 12px;
  left: 12px;
}
</style>