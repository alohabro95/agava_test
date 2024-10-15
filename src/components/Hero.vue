<script setup>
const props = defineProps({
  caption: String,
  lemon: String,
  img1: String,
  img2: String,
  img3: String,
});
</script>

<template>
  <main>
    <div class="hero">
      <div class="hero-container">
        <h2 class="hero__caption hero__caption--gray">{{ props.caption }}</h2>
        <div class="lemon-container">
          <h2 class="hero__caption hero__caption--lemon">
            {{ props.lemon }}
          </h2>
          <h2 class="lemon-clone">{{ props.lemon }}</h2>
        </div>
        <button class="hero__button">
          <span class="button-text">SOLOSIDI SEM</span>
        </button>
        <img :src="props.img1" alt="" class="hero__img hero__img--top" />
        <img :src="props.img2" alt="" class="hero__img hero__img--bottom" />
        <img :src="props.img3" alt="" class="hero__img hero__img--arrow" />
      </div>
    </div>
  </main>
</template>

<style lang="scss">
.hero {
  position: relative;
  border-radius: 32px;
  box-shadow: 0px 3px 4px rgba(0, 0, 0, 0.25);

  .hero-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 12px;
    justify-content: flex-start;
    background: linear-gradient(
      45deg,
      rgb(202, 53, 155) 0%,
      rgb(138, 43, 187) 100%
    );
    padding: 21px 0px 33px 28px;
    border-radius: 32px;
    box-shadow: inset 0px 15px 4px rgba(195, 84, 177, 0.25),
      inset 0px -15px 4px rgba(195, 84, 177, 0.25),
      inset 15px 0px 4px rgba(195, 84, 177, 0.25),
      inset -15px 0px 4px rgba(195, 84, 177, 0.25);
  }
  &__caption {
    font-size: 22px;
    &--gray {
      background: linear-gradient(0deg, #999999 28%, #ffffff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      white-space: pre-wrap;
    }

    &--lemon {
      line-height: 30px;
      z-index: 1;
      position: relative;
      max-width: 216px;
      background: linear-gradient(0deg, #ffdf8e 28%, #ffc700 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      position: relative;
    }
  }
  .lemon-container {
    position: relative;
    .lemon-clone {
      color: #000000;
      z-index: 0;
      position: absolute;
      top: 2px;
      font-size: 22px;
      max-width: 218px;
      opacity: 0.3;
    }
  }
  &__button {
    position: relative;
    font-size: 20px;
    color: #ffffff;
    padding: 4px 18px;
    background-color: #39dd00;
    border-style: none;
    border-radius: 10px;
    box-shadow: inset 0px 8px 4px rgba(255, 255, 255, 0.3),
      inset 0px -8px 4px rgba(255, 255, 255, 0.3),
      inset 8px 0px 4px rgba(255, 255, 255, 0.3),
      inset -8px 0px 4px rgba(255, 255, 255, 0.3);
    box-shadow: 0px 3px 2px rgba(0, 0, 0, 0.3);

    .button-text {
      font-weight: bold;
      background-color: rgba(0, 0, 0, 0.5);
      color: transparent;
      text-shadow: 0.7px 0.7px 1.5px rgba(255, 255, 255);
      -webkit-background-clip: text;
      -moz-background-clip: text;
      background-clip: text;
    }
  }

  &__img {
    &--top {
      top: -38px;
      right: 0px;
      z-index: 1;
      position: absolute;
    }

    &--bottom {
      bottom: -54px;
      right: 0px;
      z-index: 1;
      position: absolute;
    }
  }
}
@media screen and (min-width: 600px) {
  .hero {
    .hero-container {
      gap: 20px;
      padding: 40px 0px 40px 38px;
    }
    &__caption {
      font-size: 32px;
      white-space: unset;

      &--lemon {
        max-width: unset;
      }
    }
    .lemon-container {
      .lemon-clone {
        top: -4px;
        font-size: 32px;
        max-width: unset;
      }
    }
    &__button {
      width: 209px;
      font-size: 24px;
      padding: 8px 34px;
      border-radius: 13px;
    }
    // &__img {
    //   &--top {
    //     top: -38px;
    //     right: 0px;
    //     z-index: 1;
    //     position: absolute;
    //   }
    //   &--bottom {
    //     bottom: -54px;
    //     right: 0px;
    //     z-index: 1;
    //     position: absolute;
    //   }
    // }
  }
  .comp__hero1 {
    .hero__img--top {
      content: url(../assets/images/desktop_images/hero/hero-desktop-left.png);
      width: 94px;
      height: 102px;
      right: 60px;
    }
    .hero__img--bottom {
      content: url(../assets/images/desktop_images/hero/hero-desktop-right.png);
      right: 58px;
      width: 150px;
      height: 162px;
    }
  }
  .section-mauris {
    .comp__hero2 {
      .hero__img--top {
        width: 130px;
        height: 140px;
        top: -84px;
        content: url(../assets/images/desktop_images/hero/hero2-desktop-top.png);
      }
      .hero__img--bottom {
        content: url(../assets/images/desktop_images/hero/hero2-desktop-bottom.png);

        right: 60px;
        bottom: -78px;
        width: 170px;
        height: 186px;
      }
    }
  }
  .section-etiam {
    .comp__hero3 {
      .hero__img--top {
        content: url(../assets/images/desktop_images/hero/hero3-desktop-top.png);
        top: -146px;
        right: 213px;
      }
      .hero__img--arrow {
        content: url(../assets/images/desktop_images/hero/hero3-desktop-arrow.png);
        top: -44px;
        right: 150px;
      }
      .hero__img--bottom {
        content: url(../assets/images/desktop_images/hero/hero3-desktop-bottom.png);
        bottom: -64px;
        right: 58px;
        width: 251px;
        height: 205px;
      }
    }
  }
}
@media screen and (min-width: 1280px) {
  .hero {
    .hero-container {
      gap: unset;
      padding: 44px 0px 46px 48px;
    }
    &__caption {
      font-size: 32px;
      white-space: unset;

      &--lemon {
        font-size: 54px;
        max-width: unset;
        line-height: normal;
        margin-bottom: 20px;
      }
    }
    .lemon-container {
      .lemon-clone {
        top: 7px;
        font-size: 54px;
        max-width: unset;
      }
    }
    &__button {
      width: unset;
      font-size: 40px;
      padding: 8px 62px;
      border-radius: 13px;
    }
    &__img {
      &--top {
        top: -38px;
        right: 0px;
        z-index: 1;
        position: absolute;
      }
      &--bottom {
        bottom: -54px;
        right: 0px;
        z-index: 1;
        position: absolute;
      }
    }
  }
}
@media screen and (min-width: 1440px) {
  .comp__hero1 {
    .hero__img--top {
      width: 232px;
      height: 251px;
      right: 380px;
    }
    .hero__img--bottom {
      right: 58px;
      width: 376px;
      height: 407px;
    }
  }
  .section-mauris {
    .comp__hero2 {
      .hero__img--top {
        width: 52%;
        height: 100%;
        top: -5px;
        content: url(/src/assets/images/desktop_images/hero/hero2-desktopFull.png);
      }
      .hero__img--bottom {
        display: none;
        content: url(../assets/images/desktop_images/hero/hero2-desktop-bottom.png);

        right: 60px;
        bottom: -78px;
        width: 170px;
        height: 186px;
      }
    }
    .hero__caption--gray {
      margin-bottom: 20px;
      order: 2;
    }
    .lemon-container {
      .hero__caption--lemon {
        margin-bottom: unset;
      }
      order: 1;
    }
    .hero__button {
      order: 3;
    }
  }
  .section-etiam {
    .comp__hero3 {
      .hero-container {
        .lemon-container {
          width: 375px;
        }
      }
      .hero__img--top {
        content: url(../assets/images/desktop_images/hero/hero3-desktopFull.png);
        width: 80%;
        top: -20px;
        right: -25px;
      }
      .hero__img--arrow {
        display: none;
        content: url(../assets/images/desktop_images/hero/hero3-desktop-arrow.png);
        top: -44px;
        right: 150px;
      }
      .hero__img--bottom {
        display: none;
        content: url(../assets/images/desktop_images/hero/hero3-desktop-bottom.png);
        bottom: -64px;
        right: 58px;
        width: 251px;
        height: 205px;
      }
    }
  }
}
</style>
