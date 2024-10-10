<script setup>
const props = defineProps({
  review: { type: Object, required: true },
});
</script>
<template>
  <div class="reviews__item">
    <div class="reviews__header">
      <img
        class="reviews__profile"
        src="../assets/images/mobile_images/reviews/reviews__profile.png"
        alt=""
      />
      <div class="reviews__info">
        <h4 class="reviews__name">{{ review.name }}</h4>
        <span class="reviews__data">{{ review.data }}</span>
      </div>
      <div class="reviews__stars">
        <svg
          v-for="n in 5"
          :key="'star-' + n"
          width="15"
          height="15"
          viewBox="0 0 15 15"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
          class="star"
          :class="{ filled: n <= review.grade }"
        >
          <path
            d="M9.78748 9.44631L11.0105 13.379L7.86471 10.9741L7.50031 10.6956L7.13591 10.9741L3.99008 13.379L5.21314 9.44631L5.338 9.04484L5.00326 8.79043L1.78107 6.34157H5.72891H6.17171L6.30225 5.91846L7.50031 2.03521L8.69838 5.91846L8.82892 6.34157H9.27171H13.2191L9.99733 8.79046L9.66263 9.04486L9.78748 9.44631Z"
            stroke="#FFF853"
            stroke-width="1.2"
          />
        </svg>
      </div>
    </div>
    <p class="reviews__text">{{ review.text }}</p>
    <div class="reviews__footer">
      <div class="reviews__like">
        <img
          src="../assets/images/mobile_images/reviews/reviews__like.png"
          alt=""
        />
        <span>HILFREICH</span>
      </div>
      <div class="reviews__comment">
        <img
          src="../assets/images/mobile_images/reviews/reviews__comment.png"
          alt=""
        />
        <span>KOMMENTAR</span>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.reviews__item {
  display: flex;
  flex-direction: column;
  gap: 25px;
  padding: 22px;
  background-color: rgba(92, 92, 92, 0.6);
  border-radius: 30px;
}
.reviews__header {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}

.reviews__name,
.reviews__data,
.reviews__text {
  font-family: "Ubuntu", sans-serif;
}
.reviews__info {
  display: flex;
  flex-direction: column;
}
.reviews__name {
  font-size: 18px;
}
.reviews__data {
  color: #b6b6b6;
  font-size: 15px;
}
.reviews__text {
  font-size: 15px;
}
.reviews {
  &__stars {
    display: flex;
    gap: 5px;
  }
}

.star {
  &.filled {
    fill: #fff853;
  }
}
.reviews__footer {
  display: flex;
  justify-content: end;
  gap: 20px;
  div {
    display: flex;
    align-items: baseline;
    gap: 8px;
    span {
      font-size: 15px;
      color: #b6b6b6;
    }
  }
  img {
    width: 17px;
    height: 17px;
  }
}
@media screen and (min-width: 600px) {
  .reviews__item {
    padding: 24px 37px 28px 38px;
    .reviews__header {
      justify-content: flex-start;
    }
    .reviews__profile {
      margin-right: 20px;
    }
    .reviews__data,
    .reviews__text {
      font-size: 16px;
    }
    .reviews__stars {
      margin-left: auto;
      svg {
        width: 23px;
        height: 23px;
      }
    }
    .answer {
      padding: 100px;
      .reviews__header {
        gap: 0;
      }
    }
  }
}
</style>
