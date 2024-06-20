<template>
  <li class="card">
    <div class="card__img">
      <HitComponent :isActive="card.isHit"></HitComponent>
      <SvgSprite :name="card.img"></SvgSprite>
      <DiscountComponent :discount="card.discount"></DiscountComponent>
    </div>
    <div class="card__description">
      <span>{{ card.title }}</span>
      <p>{{ card.description }}</p>
    </div>
    <div class="card__price" v-if="card.isAvailable">
      <span>{{ card.discountPrice }}</span>
      <span>{{ card.fullPrice }}</span>
    </div>
    <ButtonComponent v-if="card.isAvailable" class="card__button">Купить</ButtonComponent>
    <ButtonComponent v-else class="card__button card__button--mod">Сообщить о поступлении</ButtonComponent>
  </li>
</template>

<script>
import ButtonComponent from '@/components/ui/ButtonComponent.vue';
import DiscountComponent from '@/components/ui/DiscountComponent.vue';
import HitComponent from '@/components/ui/HitComponent.vue';
import SvgSprite from '@/components/ui/SvgSprite.vue';

export default {
  props: {
    card: {
      type: Object,
      required: true
    }
  },
  components: { HitComponent, SvgSprite, DiscountComponent, ButtonComponent }
}
</script>

<style lang="scss">
.card {
  display: flex;
  flex-direction: column;
  gap: 12px
}

.card__img {
  width: 100%;
  height: 200px;
  background-color: #F8F8FA;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.card__description span {
  color: $color-font-second;
  display: block;
  margin-bottom: 8px;
}

.card__description p {
  &:hover {
    color: $color-font-hover;
  }
}

.card__price {
  display: flex;
  gap: 4px;
  align-items: center;
}

.card__price span:first-child {
  font-weight: 700;
  font-size: 16px;
  line-height: 14px;
}

.card__price span:last-child {
  color: $color-font-second;
  font-size: 12px;
  line-height: 14px;
  text-decoration: line-through;
}
</style>