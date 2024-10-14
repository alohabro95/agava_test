<script lang="ts" setup>
import "v-slick-carousel/style.css";
import { VSlickCarousel } from "v-slick-carousel";

const settings = {
  groupsToShow: 1,
  groupsToScroll: 1,
  arrows: true,
  infinite: true,
};
</script>

<template>
  <div class="carousel carousel1">
    <VSlickCarousel v-bind="settings">
      <div class="tema">
        <div class="slider-item">
          <div>
            <img
              src="../assets/images/mobile_images/slider/1.png"
              alt="slider image 1"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/2.png"
              alt="slider image 2"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/3.png"
              alt="slider image 3"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/4.png"
              alt="slider image 4"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/5.png"
              alt="slider image 5"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/6.png"
              alt="slider image 6"
            />
          </div>
        </div>
      </div>
      <div class="tema">
        <div class="slider-item">
          <div>
            <img
              src="../assets/images/mobile_images/slider/1.png"
              alt="slider image 1"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/2.png"
              alt="slider image 2"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/3.png"
              alt="slider image 3"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/4.png"
              alt="slider image 4"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/5.png"
              alt="slider image 5"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/6.png"
              alt="slider image 6"
            />
          </div>
        </div>
      </div>
      <div class="tema">
        <div class="slider-item">
          <div>
            <img
              src="../assets/images/mobile_images/slider/1.png"
              alt="slider image 1"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/2.png"
              alt="slider image 2"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/3.png"
              alt="slider image 3"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/4.png"
              alt="slider image 4"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/5.png"
              alt="slider image 5"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/6.png"
              alt="slider image 6"
            />
          </div>
        </div>
      </div>
      <template #prevArrow="arrowSlotProps">
        <button
          class="slider-arrow slider-arrow--left"
          @click="arrowSlotProps.onClick"
        >
          <img
            src="../assets/images/mobile_images/slider/slider-arrow-left.png"
            alt="Previous"
          />
        </button>
      </template>
      <template #nextArrow="arrowSlotProps">
        <button
          class="slider-arrow slider-arrow--right"
          @click="arrowSlotProps.onClick"
        >
          <img
            src="../assets/images/mobile_images/slider/slider-arrow-right.png"
            alt="Previous"
          />
        </button>
      </template>
    </VSlickCarousel>
  </div>
  <div class="carousel2">
    <VSlickCarousel v-bind="settings">
      <div class="tema">
        <div class="slider-item">
          <div>
            <img
              src="../assets/images/mobile_images/slider/1.png"
              alt="slider image 1"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/4.png"
              alt="slider image 4"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/5.png"
              alt="slider image 5"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/6.png"
              alt="slider image 6"
            />
          </div>
        </div>
      </div>
      <div class="tema">
        <div class="slider-item">
          <div>
            <img
              src="../assets/images/mobile_images/slider/1.png"
              alt="slider image 1"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/4.png"
              alt="slider image 4"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/5.png"
              alt="slider image 5"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/6.png"
              alt="slider image 6"
            />
          </div>
        </div>
      </div>
      <div class="tema">
        <div class="slider-item">
          <div>
            <img
              src="../assets/images/mobile_images/slider/1.png"
              alt="slider image 1"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/4.png"
              alt="slider image 4"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/5.png"
              alt="slider image 5"
            />
          </div>
          <div>
            <img
              src="../assets/images/mobile_images/slider/6.png"
              alt="slider image 6"
            />
          </div>
        </div>
      </div>
      <template #prevArrow="arrowSlotProps">
        <button
          class="slider-arrow slider-arrow--left"
          @click="arrowSlotProps.onClick"
        >
          <img
            src="../assets/images/mobile_images/slider/slider-arrow-left.png"
            alt="Previous"
          />
        </button>
      </template>
      <template #nextArrow="arrowSlotProps">
        <button
          class="slider-arrow slider-arrow--right"
          @click="arrowSlotProps.onClick"
        >
          <img
            src="../assets/images/mobile_images/slider/slider-arrow-right.png"
            alt="Previous"
          />
        </button>
      </template>
    </VSlickCarousel>
  </div>
</template>

<style lang="scss">
.tema {
  margin-bottom: 60px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  column-gap: 10px;
  gap: 7px;
  img {
    font-size: 0;
    margin: 0;
  }
}
.slider-item {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  row-gap: 7px;
  column-gap: 11px;
  div {
    max-height: 146px;
    width: fit-content;
    margin: 0;
  }
}
.buttons {
  display: flex;
  justify-content: center;
  gap: 38px;
}
.slider-arrow {
  position: absolute;
  background: none;
  border: none;
  cursor: pointer;
  img {
    transition: all 1s ease;
  }
  img:hover {
    transform: scale(0.9);
  }
  &--right {
    right: 47%;
    bottom: 0;
    transform: translateX(100%);
  }
  &--left {
    transform: translateX(-100%);
    left: 47%;
    bottom: 0;
    z-index: 1;
  }
}
@media screen and (max-width: 767px) {
  .carousel2 {
    display: none;
  }
}
@media screen and (min-width: 768px) {
  .carousel1 {
    display: none;
  }
  .carousel2 {
    .v-slick-track {
      height: 340px;
    }
    .slider-item {
      display: flex;
      img {
        min-width: 170px;
        min-height: 240px;
      }
    }
  }
  .slider-arrow {
    img {
      min-width: 54px;
      min-height: 54px;
    }
  }
}
</style>
