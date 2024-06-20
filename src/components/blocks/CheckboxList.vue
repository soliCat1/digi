<template>
  <ul>
    <CheckboxComponent v-for="(attribute, index) in attributes" :key="index" :attribute="attribute"></CheckboxComponent>
  </ul>
</template>

<script>
import CheckboxComponent from '@/components/ui/CheckboxComponent.vue';

export default {
  components: { CheckboxComponent },
  props: {
    attributes: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 12px;
  overflow-y: scroll;
  height: 180px;
}

ul::-webkit-scrollbar {
  width: 6px;
}

ul::-webkit-scrollbar-thumb {
  border-radius: 10px;
  background-color: $scroll-bar;
  cursor: pointer;
}

ul::-webkit-scrollbar-track {
  border-radius: 10px;
  background-color: transparent;
}
</style>