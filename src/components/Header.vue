<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import Menu from "./Menu.vue";

const mainMenu = {
  number1: [
    {
      key: "Pidorsk",
      tooltipText: "Pidorsk Tooltip",
      img: new URL(
        "../assets/images/mobile_images/burger-list/check.png",
        import.meta.url
      ).href,
    },
    {
      key: "Home",
      tooltipText: "Home",
      img: new URL(
        "../assets/images/mobile_images/burger-list/home.png",
        import.meta.url
      ).href,
    },
  ],
  number2: [
    {
      key: "Stock",
      tooltipText: "Stock",
      img: new URL(
        "../assets/images/mobile_images/burger-list/stock.png",
        import.meta.url
      ).href,
    },
    {
      key: "User",
      tooltipText: "User",
      img: new URL(
        "../assets/images/mobile_images/burger-list/user.png",
        import.meta.url
      ).href,
    },
    {
      key: "Stock",
      tooltipText: "Dollar",
      img: new URL(
        "../assets/images/mobile_images/burger-list/dollar.png",
        import.meta.url
      ).href,
    },
  ],
  number3: [
    {
      key: "Eye",
      tooltipText: "Eye",
      img: new URL(
        "../assets/images/mobile_images/burger-list/eye.png",
        import.meta.url
      ).href,
    },
    {
      key: "Call",
      tooltipText: "Call",
      img: new URL(
        "../assets/images/mobile_images/burger-list/call.png",
        import.meta.url
      ).href,
    },
    {
      key: "Phone",
      tooltipText: "Phone",
      img: new URL(
        "../assets/images/mobile_images/burger-list/phone.png",
        import.meta.url
      ).href,
    },
  ],
  number4: [
    {
      key: "Questions",
      tooltipText: "Questions",
      img: new URL(
        "../assets/images/mobile_images/burger-list/questions.png",
        import.meta.url
      ).href,
    },
    {
      key: "Cloud",
      tooltipText: "Cloud",
      img: new URL(
        "../assets/images/mobile_images/burger-list/cloud.png",
        import.meta.url
      ).href,
    },
  ],
};

const isOpen = ref(false);

const toggleMenu = () => {
  if (window.innerWidth < 1440) {
    isOpen.value = !isOpen.value;
  }
};

const updateMenuDisplay = () => {
  if (window.innerWidth >= 1440) {
    isOpen.value = true;
  } else {
    isOpen.value = false;
  }
};

onMounted(() => {
  window.addEventListener("resize", updateMenuDisplay);
  updateMenuDisplay();
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", updateMenuDisplay);
});
</script>

<template>
  <section class="section-header">
    <div class="header">
      <button
        @click="toggleMenu"
        :class="{ active: isOpen }"
        class="burger-button"
      >
        <span class="burger__icon" :class="{ active: isOpen }"></span>
        <span class="burger__icon" :class="{ active: isOpen }"></span>
        <span class="burger__icon" :class="{ active: isOpen }"></span>
      </button>
      <nav v-if="isOpen" class="burger__menu">
        <ul class="burger__list">
          <li class="list-el">
            <Menu :options="mainMenu.number1" />
          </li>
          <li class="list-el">
            <Menu :options="mainMenu.number2" />
          </li>
          <li class="list-el">
            <Menu :options="mainMenu.number3" />
          </li>
          <li class="list-el">
            <Menu :options="mainMenu.number4" />
          </li>
        </ul>
      </nav>
      <div class="logo-group">
        <img
          class="logo-image"
          src="../assets/images/mobile_images/header_logo.png"
          alt=""
        />
        <div class="captions">
          <img
            class="captions__image captions__image--big"
            src="../assets/images/table_images/kalina.png"
            alt=""
          />
          <img
            class="captions__image captions__image--big"
            src="../assets/images/table_images/casino.png"
            alt=""
          />
          <img
            class="captions__image captions__image--small"
            src="../assets/images/table_images/review.png"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&display=swap");
body {
  // background-image: url(../assets/images/mobile_images/background1.png);
  background-color: #432488;
  background-repeat: repeat;
}
.section-header {
  margin-bottom: 44px;
  background-color: #432488;
  position: relative;
  padding: 0;

  .header {
    position: relative;
    display: flex;
    justify-content: space-between;
    padding: 12px 16px;
    align-items: center;

    .burger-button {
      padding: 0;
      background: none;
      border: none;
      cursor: pointer;
      display: flex;
      gap: 5px;
      flex-direction: column;
      transition: 0.8s ease;
      &:hover {
        transform: scale(0.9);
      }
      .burger__icon {
        width: 27px;
        height: 3px;
        background-color: #d536ff;
        border: 1px solid #3c004c;
        border-radius: 12px;
        transition: all 0.3s ease;
        box-shadow: 0px 0px 6px 0px #ffffff26;
      }
    }
    .burger__menu {
      z-index: 2;
      position: absolute;
      top: calc(100% + 20px);
    }
    .burger__list {
      z-index: 2;
      background-color: transparent;
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .logo-group {
      display: flex;
      max-height: 23px;
      gap: 7px;
    }
    .captions {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      height: 23px;
      overflow: hidden;
      align-items: flex-start;
      &__image {
        &--big {
          max-height: 7px;
        }
        &--small {
          max-height: 5px;
        }
      }
    }
  }
}
@media screen and (min-width: 600px) {
  .section-header {
    margin-bottom: 62px;
    .header {
      padding: 15px 30px;
      .burger-button {
        gap: 8px;
        .burger__icon {
          width: 40px;
        }
      }
      .logo-group {
        max-height: unset;
        .logo-image {
          content: url(../assets/images/table_images/header_logo.png);
        }
        .captions {
          height: unset;
          overflow: hidden;
          align-items: flex-start;
          &__image {
            &--big {
              max-height: 11px;
            }
            &--small {
              max-height: 7px;
            }
          }
        }
      }
    }
  }
}
@media screen and (min-width: 1280px) {
  .section-header {
    margin-bottom: 130px;
  }
}
@media screen and (min-width: 1440px) {
  .section-header {
    .header {
      .burger-button {
        order: 2;
        display: none;
      }
      .burger__menu {
        position: absolute;
        top: calc(100% + 27px);
        order: 3;
      }
      .logo-group {
        order: 1;
      }
    }
  }
}
</style>
