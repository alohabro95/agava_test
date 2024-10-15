<script setup>
import { ref } from "vue";

const isOpen = ref(false);
const currentTooltip = ref(null);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};

const showTooltip = (tooltipText) => {
  currentTooltip.value = tooltipText;
};

const hideTooltip = () => {
  currentTooltip.value = null;
};
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
            <ul class="menu">
              <li @mouseover="showTooltip('Pidorsk')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/check.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Pidorsk'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Pidorsk</div>
                </div>
              </li>
              <li @mouseover="showTooltip('Home')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/home.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Home'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Home</div>
                </div>
              </li>
            </ul>
          </li>
          <li class="list-el">
            <ul class="menu">
              <li @mouseover="showTooltip('Stock')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/stock.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Stock'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Stock</div>
                </div>
              </li>
              <li @mouseover="showTooltip('User')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/user.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'User'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">User</div>
                </div>
              </li>
              <li @mouseover="showTooltip('Dollar')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/dollar.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Dollar'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Dollar</div>
                </div>
              </li>
            </ul>
          </li>
          <li class="list-el">
            <ul>
              <li @mouseover="showTooltip('Eye')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/eye.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Eye'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Eye</div>
                </div>
              </li>
              <li @mouseover="showTooltip('Call')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/call.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Call'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Call</div>
                </div>
              </li>
              <li @mouseover="showTooltip('Phone')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/phone.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Phone'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Phone</div>
                </div>
              </li>
            </ul>
          </li>
          <li class="list-el">
            <ul>
              <li
                @mouseover="showTooltip('Questions')"
                @mouseleave="hideTooltip"
              >
                <img
                  src="../assets/images/mobile_images/burger-list/questions.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Questions'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Questions</div>
                </div>
              </li>
              <li @mouseover="showTooltip('Cloud')" @mouseleave="hideTooltip">
                <img
                  src="../assets/images/mobile_images/burger-list/cloud.png"
                  alt=""
                />
                <div v-if="currentTooltip === 'Cloud'" class="tooltip">
                  <div class="tooltip-arrow"></div>
                  <div class="tooltip-text">Cloud</div>
                </div>
              </li>
            </ul>
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

    .burger__list {
      z-index: 2;
      max-width: 30px;
      background-color: transparent;
      position: absolute;
      top: 110%;
      left: 12px;
      right: 0;
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 12px;
      ul {
        display: flex;
        flex-direction: column;
        gap: 3px;
        list-style: none;
        padding: 0;
        margin: 0;
        li {
          cursor: pointer;
          position: relative;
          display: flex;
          justify-content: center;
          align-items: center;
          width: 35px;
          height: 35px;
          border-radius: 5px;
          background-color: #432488;
          transition: 0.5s ease;
          &:hover {
            background-color: #d536ff;
          }
          &:hover .tooltip {
            opacity: 1;
          }

          .tooltip {
            display: flex;
            align-items: center;
            position: absolute;
            left: 150%;
            top: 50%;
            transform: translateY(-50%);
            opacity: 0;
            transition: opacity 0.3s ease;
          }

          .tooltip-text {
            background-color: #d9d9d9;
            padding: 5px 10px;
            white-space: nowrap;
            color: #6d1373;
          }

          .tooltip-arrow {
            width: 0;
            height: auto;
            border-style: solid;
            border-width: 17px 23px 17px 0;
            border-color: transparent #d9d9d9 transparent transparent;
          }
        }
      }
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
      .burger__list {
        top: 110%;
        left: 30px;
        ul {
          li {
            width: 40px;
            height: 40px;
          }
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
</style>
