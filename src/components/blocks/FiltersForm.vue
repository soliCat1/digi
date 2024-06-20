<template>
  <form>
    <fieldset>
      <LegendComponent>Цена</LegendComponent>
      <div class="price__container">
        <PriceInput>от</PriceInput>
        <div class="price__border"></div>
        <PriceInput>до</PriceInput>
      </div>
    </fieldset>
    <fieldset>
      <LegendComponent class="brand">
        Бренд
        <ButtonComponent type="reset" class="filters-reset">Очистить</ButtonComponent>
      </LegendComponent>
      <FiltersSearch></FiltersSearch>
      <CheckboxList :attributes="brandAttributes"></CheckboxList>
    </fieldset>
    <fieldset>
      <LegendComponent>Размер</LegendComponent>
      <CheckboxList :attributes="sizeAttributes"></CheckboxList>
    </fieldset>
  </form>
</template>

<script>
import FiltersSearch from '@/components/ui/FiltersSearch.vue';
import LegendComponent from '@/components/ui/LegendComponent.vue';
import PriceInput from '@/components/ui/PriceInput.vue';
import ButtonComponent from '@/components/ui/ButtonComponent.vue';
import CheckboxList from '@/components/blocks/CheckboxList.vue';

export default {
  components: { FiltersSearch, LegendComponent, PriceInput, ButtonComponent, CheckboxList },
  data: () => ({
    brandAttributes: [
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      }
    ],
    sizeAttributes: [
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      },
      {
        attr: "Атрибут",
        count: 3
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
form {
  display: none;

  @media (min-width: $desktop-width) {
    display: flex;
    flex-direction: column;
    gap: 28px;
  }
}

fieldset {
  padding: 0;
  border: none;
  display: flex;
  flex-direction: column;
  gap: 16px;
}


.price__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 17px;
}

.price__border{
  width: 10px;
  height: 1px;
  background-color: $color-border;
}
</style>