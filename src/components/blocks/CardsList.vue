<template>
  <ul>
    <CardComponent v-for="card in cards" :key="card.id" :card="card"></CardComponent>
  </ul>
</template>

<script>
import CardComponent from '@/components/blocks/CardComponent.vue';

export default {
  components: { CardComponent },
  data: () => ({
    cards: [
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-big'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: false,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
      {
        isHit: true,
        discount: "25%",
        title: "Бренд",
        description: "Полное название товара в несколько строк для вида с обрывом в конце...",
        discountPrice: "5 990 ₽",
        fullPrice: "5 990 ₽",
        isAvailable: true,
        img: 'box-small'
      },
    ]
  })
}
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px 12px;
  padding: 12px 0;

  @media (min-width: $desktop-width) {
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 24px 0 36px 0;
  }
}
</style>