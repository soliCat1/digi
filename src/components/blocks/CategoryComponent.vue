<template>
  <div class="category">
    <span class="category__title">Название категории <span class="category__count">3</span></span>
    <ul class="category__list">
      <li>
        Название категории <span class="category__count">3</span>
      </li>
      <li>
        Название категории <span class="category__count">3</span>
      </li>
      <li>
        Название категории <span class="category__count">3</span>
      </li>
    </ul>
  </div>
</template>

<style lang="scss">
.category__count {
  display: none;
  padding: 8px 16px;
  margin-left: auto;
  font-size: 12px;
  line-height: 14px;
  color: $color-font-second;

  @media (min-width: $desktop-width) {
    display: block;
  }
}

.category__title {
  display: block;
  font-size: 22px;
  line-height: 28px;

  @media (min-width: $desktop-width) {
    font-size: 14px;
    line-height: 16px;
  }
}

.category__title,
.category__list li {
  display: flex;
  align-items: center;
}

.category__list {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
    list-style: none;
    padding-left: 32px;
  }
}
</style>