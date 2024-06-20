<template>
  <button>
    <slot></slot>
  </button>
</template>

<style lang="scss" scoped>
button {
  border: none;
  font-family: inherit;
  padding: 0;
  cursor: pointer;
  background-color: transparent;
  transition: all 0.2s ease;
}

.reset {
  opacity: 0.3;

  &:hover {
    opacity: 1;
  }

  @media (min-width: $desktop-width) {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    right: 82px;
  }
}

.filters-reset {
  position: absolute;
  top: 2px;
  right: 0;
  text-decoration: underline;
  font-size: 12px;
  line-height: 12px;
  color: $color-font-second;

  &:hover {
    color: $color-font-main;
  }
}

.submit {
  padding: 12px 16px;
  color: $color-white;
  border-radius: 5px;
  background-color: $color-brand;
  font-size: 16px;
  line-height: 14px;

  @media (min-width: $desktop-width) {
    border-radius: 10px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    right: 4px;
  }
}

.catalog {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
    padding: 15px 24px;
    color: #000000;
    border-radius: 10px;
    border: 1px solid $color-brand;
    font-family: "Inter", sans-serif;
    font-size: 14px;
    line-height: 14px;
    font-weight: 500;
    margin-right: 24px;
  }
}

.card__button {
  padding: 12px 16px;
  color: $color-brand;
  border-radius: 5px;
  border: 1px solid $color-brand;
  font-size: 14px;
  line-height: 14px;
  font-weight: 700;
  width: fit-content;

  &:hover {
    color: $color-white;
    background-color: $color-brand;
  }

  &--mod {
    color: $color-font-second;
    border: 1px solid $color-font-second;
    margin-top: auto;
    width: 100%;
    padding: 12px 4px;

    &:hover {
      color: $color-white;
      background-color: $color-font-second;
    }
  }
}
</style>