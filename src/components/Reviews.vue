<script setup>
import CustomSelect from "./CustomSelect.vue";
import ReviewItem from "./ReviewItem.vue";
const reviews = [
  {
    name: "Ivan",
    data: "03 july, 2024",
    grade: 4,
    text: "Aenean pharetra sodales nunc, ac tincidunt metus tempus vel. Vivamus a malesuada nisi, sed facilisis velit. Proin blandit facilisis purus, euismod feugiat odio. Phasellus interdum ultrices felis vitae finibus. Sed sodales suscipit congue. Aenean ultrices non elit et eleifend. ",
  },
  {
    name: "Fedor",
    data: "5 november, 2024",
    grade: 5,
    text: "Aenean pharetra sodales nunc, ac tincidunt metus tempus vel. Vivamus a malesuada nisi, sed facilisis velit. Proin blandit facilisis purus, euismod feugiat odio. Phasellus interdum ultrices felis vitae finibus. Sed sodales suscipit congue. Aenean ultrices non elit et eleifend. ",
  },
  {
    name: "Igor",
    data: "14 march, 2024",
    grade: 3,
    text: "Aenean pharetra sodales nunc, ac tincidunt metus tempus vel. Vivamus a malesuada nisi, sed facilisis velit. Proin blandit facilisis purus, euismod feugiat odio. Phasellus interdum ultrices felis vitae finibus. Sed sodales suscipit congue. Aenean ultrices non elit et eleifend. ",
  },
  {
    name: "Pidor",
    data: "4 september, 2024",
    grade: 1,
    text: "Aenean pharetra sodales nunc, ac tincidunt metus tempus vel. Vivamus a malesuada nisi, sed facilisis velit. Proin blandit facilisis purus, euismod feugiat odio. Phasellus interdum ultrices felis vitae finibus. Sed sodales suscipit congue. Aenean ultrices non elit et eleifend. ",
  },
];
</script>
<template>
  <main>
    <div class="reviews">
      <div class="reviews__top">
        <h3 class="reviews__caption">Mauris in metus luctus</h3>
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
            :class="{ filled: n }"
          >
            <path
              d="M9.78748 9.44631L11.0105 13.379L7.86471 10.9741L7.50031 10.6956L7.13591 10.9741L3.99008 13.379L5.21314 9.44631L5.338 9.04484L5.00326 8.79043L1.78107 6.34157H5.72891H6.17171L6.30225 5.91846L7.50031 2.03521L8.69838 5.91846L8.82892 6.34157H9.27171H13.2191L9.99733 8.79046L9.66263 9.04486L9.78748 9.44631Z"
              stroke="#FFF853"
              stroke-width="1.2"
            />
          </svg>
        </div>
      </div>
      <h4 class="reviews__caption--small">*NULLA IN ULTRICIES LOREM</h4>
      <div class="reviews__sorting">
        <CustomSelect />
      </div>
      <div class="reviews__items">
        <ReviewItem
          v-for="(review, index) in reviews.slice(0, 3)"
          :key="index"
          :review="review"
        />
        <div class="reviews__item answer">
          <div class="reviews__header">
            <img
              class="reviews__profile"
              src="../assets/images/mobile_images/reviews/reviews__profile.png"
              alt=""
            />
            <div class="reviews__info">
              <h4 class="reviews__name">Vafledron</h4>
              <span class="reviews__data">15 march, 2024</span>
            </div>
          </div>
          <p class="reviews__text">
            Aenean pharetra sodales nunc, ac tincidunt metus tempus vel. Vivamus
            a malesuada nisi, sed facilisis velit. Proin blandit facilisis
            purus, euismod feugiat odio.
          </p>
        </div>
        <div class="reviews__item forms">
          <div class="forms__header">
            <h4 class="forms__caption reviews__caption--h4">
              HINTERLASSEN SIE EINE BEWERTUNG
            </h4>
            <div class="reviews__stars forms__stars">
              <svg
                v-for="n in 5"
                :key="'star-' + n"
                width="15"
                height="15"
                viewBox="0 0 15 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="star"
              >
                <path
                  d="M9.78748 9.44631L11.0105 13.379L7.86471 10.9741L7.50031 10.6956L7.13591 10.9741L3.99008 13.379L5.21314 9.44631L5.338 9.04484L5.00326 8.79043L1.78107 6.34157H5.72891H6.17171L6.30225 5.91846L7.50031 2.03521L8.69838 5.91846L8.82892 6.34157H9.27171H13.2191L9.99733 8.79046L9.66263 9.04486L9.78748 9.44631Z"
                  stroke="#FFF853"
                  stroke-width="1.2"
                />
              </svg>
            </div>
          </div>
          <textarea class="forms__textarea" name="" id=""></textarea>
          <div class="forms__group">
            <input class="forms__input" type="text" placeholder="IHR NAME*" />
            <div class="forms__checkbox">
              <label class="custom-checkbox">
                <input type="checkbox" />
                <span class="checkmark"></span>
                ICH BIN KEIN ROBOTER
              </label>
            </div>
            <button class="forms__btn">FEEDBACK SENDEN</button>
          </div>
        </div>
        <div class="reviews__more">
          <ReviewItem :review="reviews[3]" />
          <div class="more-overlay">
            <div class="overlay__other">
              <img
                src="../assets/images/mobile_images/reviews/reviews__arrow.png"
                alt=""
                width="15px"
                height="15px"
              />
              <h3>MORE</h3>
              <img
                src="../assets/images/mobile_images/reviews/reviews__arrow.png"
                alt=""
                width="15px"
                height="15px"
              />
            </div>
          </div>
        </div>
        <div class="reviews__item forms forms--full">
          <div class="forms__header">
            <h4 class="forms__caption reviews__caption--h4">
              Hinterlassen Sie eine Bewertung
            </h4>
            <div class="reviews__stars forms__stars">
              <svg
                v-for="n in 5"
                :key="'star-' + n"
                width="15"
                height="15"
                viewBox="0 0 15 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="star"
              >
                <path
                  d="M9.78748 9.44631L11.0105 13.379L7.86471 10.9741L7.50031 10.6956L7.13591 10.9741L3.99008 13.379L5.21314 9.44631L5.338 9.04484L5.00326 8.79043L1.78107 6.34157H5.72891H6.17171L6.30225 5.91846L7.50031 2.03521L8.69838 5.91846L8.82892 6.34157H9.27171H13.2191L9.99733 8.79046L9.66263 9.04486L9.78748 9.44631Z"
                  stroke="#FFF853"
                  stroke-width="1.2"
                />
              </svg>
            </div>
          </div>
          <textarea class="forms__textarea" name="" id=""></textarea>
          <div class="forms__group">
            <input class="forms__input" type="text" placeholder="Ihr Name*" />
            <div class="forms__checkbox">
              <label class="custom-checkbox">
                <input type="checkbox" />
                <span class="checkmark"></span>
                Ich bin kein Roboter
              </label>
            </div>
            <button class="forms__btn">FEEDBACK SENDEN</button>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap");
.reviews {
  &__more {
    position: relative;
  }
}
.more-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    180deg,
    rgba(158, 158, 158, 0.2) 0%,
    #442a4c 67.82%
  );
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 30px;
}
.overlay__other {
  display: flex;
  position: absolute;
  bottom: 33px;
  left: 36%;
  align-items: baseline;
  gap: 7px;
  h3 {
    font-family: "Ubuntu", sans-serif;
  }
}

.reviews {
  display: flex;
  flex-direction: column;
  gap: 16px;
  &__top,
  &__middle,
  &__nunc {
    display: flex;
    align-items: baseline;
  }
  &__top {
    gap: 10px;
  }

  &__caption {
    &--regular {
      font-weight: 500;
    }
    &--small {
      font-size: 14px;
    }
  }
  &__nunc {
    gap: 3px;
    border: 2px #d536ff solid;
    padding: 8px;
    border-radius: 10px;
  }
  &__arrow {
    background-color: unset;
    border-style: none;
  }
  &__items {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }
  .answer,
  .forms {
    width: 70%;
    margin-left: auto;
    gap: 20px;
    &--full {
      width: auto;
      margin-left: unset;
      font-size: 20px;
    }
    &__header {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__caption {
      font-family: "Ubuntu", sans-serif;
      font-weight: 500;
      white-space: nowrap;
    }
    .reviews__stars {
      justify-content: flex-end;
      svg {
        width: 20px;
        height: 20px;
      }
    }
    .forms__group {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__checkbox,
    &__textarea,
    &__input {
      resize: none;
      background: none;
      border-style: none;
      border: 1px #d536ff solid;
    }
    &__textarea {
      border-radius: 12px;
      height: 117px;
    }
    &__input {
      padding: 10px 0px 10px 25px;
      font-family: "Montserrat", sans-serif;
      border-radius: 10px;
    }
  }
  .forms__checkbox {
    padding: 6px 28px;
    border-radius: 10px;
    .custom-checkbox input {
      position: absolute;
      opacity: 0;
      cursor: pointer;
    }
    .custom-checkbox {
      font-family: "Ubuntu";
      display: inline-block;
      position: relative;
      padding-left: 30px;
      cursor: pointer;
      font-size: 16px;
      user-select: none;
    }

    .custom-checkbox .checkmark {
      position: absolute;
      top: -2px;
      left: 0;
      height: 20px;
      width: 20px;
      background: none;
      border: 1px solid #d536ff;
      border-radius: 5px;
      transition: background-color 0.2s;
    }

    .custom-checkbox:hover input ~ .checkmark {
      background-color: #470259;
    }

    .custom-checkbox input:checked ~ .checkmark {
      background-color: #470259;
    }

    .custom-checkbox .checkmark::after {
      content: url(../assets/images/mobile_images/galochka.svg);
      position: absolute;
      display: none;
      right: -1px;
    }

    .custom-checkbox input:checked ~ .checkmark::after {
      display: block;
    }
  }
  .forms__btn {
    display: inline;
    font-family: "Ubuntu", sans-serif;
    font-size: 17px;
    font-weight: 700;
    padding: 10px 42px;
    background-color: #9a38b4;
    border-style: solid;
    border-width: 1px;
    border-radius: 10px;
    white-space: nowrap;
  }
}
@media screen and (min-width: 600px) {
  .reviews {
    &__top {
      gap: 40px;
      align-items: center;
      margin-bottom: 13px;
    }
    &__caption {
      font-size: 25px;
      &--small {
        font-size: 18px;
        margin-bottom: 30px;
      }
    }
    &__stars {
      svg {
        width: 30px;
        height: 30px;
      }
    }
    &__sorting {
      margin-bottom: 48px;
    }
    &__items {
      gap: 30px;
    }
  }
  .answer {
    .reviews__header {
      gap: 0;
    }
  }
  .forms {
    width: 70%;
    margin-left: auto;
    gap: 30px;
    flex-direction: unset;
    flex-wrap: wrap;
    &--full {
      width: auto;
      margin-left: unset;
      font-size: 20px;
    }
    .forms__header {
      width: 100%;
      flex-direction: row;
      justify-content: space-between;
    }
    &__caption {
      font-size: 18px;
    }
    .reviews__stars {
      svg {
        width: 20px;
        height: 20px;
      }
    }
    .forms__group {
      order: 2;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__textarea {
      flex: 1;
      height: auto;
      order: 3;
    }
  }
  .overlay__other {
    bottom: 33px;
    left: 42%;
    gap: 4px;
    h3 {
      font-size: 25px;
    }
    img {
      width: 19px;
      height: 19px;
    }
  }
}
@media screen and (min-width: 1440px) {
  .reviews {
    .reviews__items {
      .forms {
        padding: 40px 60px 60px 40px;
        .forms__header {
          align-items: end;
          flex-direction: row;
          .forms__caption {
            font-size: 25px;
          }
          svg {
            width: 40px;
            height: 40px;
          }
        }
        .forms__input,
        .forms__checkbox,
        .forms__btn,
        .forms__textarea {
          border-radius: 15px;
          font-size: 27px;
        }
        .forms__group {
          gap: 23px;
          .forms__input {
            padding: 16px 0px 16px 40px;
            font-weight: 500;
          }
          .forms__checkbox {
            align-items: center;
            .custom-checkbox {
              padding: 28px 0px 28px 64px;
              font-size: 27px;
              .checkmark {
                top: 21px;
                left: 4px;
                width: 38px;
                height: 38px;
              }
              .checkmark::after {
                right: 6px;
                top: -4px;
              }
            }
          }
          .forms__btn {
            padding: 20px 72px;
          }
        }
        .forms__textarea {
          height: unset;
        }
      }
    }
  }
}
</style>
