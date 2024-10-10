<template>
  <div class="custom-select">
    <h3 class="custom-select__label">Quisque luctus</h3>
    <div class="custom-select__input">
      <span class="custom-select__current-value">Nunc</span>
      <button class="custom-select__arrow">
        <img
          src="/src/assets/images/mobile_images/reviews/reviews__arrow.png"
          alt=""
        />
      </button>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.custom-select {
  align-items: center;
  display: flex;
  gap: 8px;
  &__label {
    font-weight: 500;
  }
  &__input {
    display: flex;
    gap: 3px;
    border: 2px #d536ff solid;
    padding: 8px;
    border-radius: 10px;
  }
  &__arrow {
    font-size: 0;
    padding: 0;
    background-color: unset;
    border-style: none;
  }
}
@media screen and (min-width: 600px) {
  .custom-select {
    gap: 11px;
    &__label {
      font-size: 25px;
    }
    &__input {
      font-size: 25px;
      align-items: baseline;
      padding: 3px 12px 5px 12px;
    }
    &__arrow {
      font-size: 0;
      padding: 0;
      background-color: unset;
      border-style: none;
    }
  }
}
</style>
