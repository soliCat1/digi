<template>
  <div class="filters">
    <CategoryComponent></CategoryComponent>
    <FiltersForm></FiltersForm>
  </div>
</template>

<script>
import CategoryComponent from '@/components/blocks/CategoryComponent.vue';
import FiltersForm from '@/components/blocks/FiltersForm.vue';

export default {
  components: { CategoryComponent, FiltersForm }
}
</script>

<style lang="scss" scoped>
.filters {
  padding: 12px 0;

  @media (min-width: $desktop-width) {
    display: flex;
    flex-direction: column;
    gap: 28px;
    padding: 24px 0 36px 0;
  }
}
</style>