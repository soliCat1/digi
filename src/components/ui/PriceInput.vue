<template>
  <div class="input__container">
    <label>
      <slot></slot>
    </label>
    <input type="number">
  </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.input__container {
  position: relative;
  width: 100%;
}

label {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  left: 8px;
  font-size: 12px;
  line-height: 14px;
  color: $color-font-second;
}

input {
  padding: 10px 26px;
  border: 1px solid $color-border;
  border-radius: 5px;
  -moz-appearance: textfield;
  width: 100%;

  &:focus {
    outline: none;
    border-color: $color-brand;
  }
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
}
</style>