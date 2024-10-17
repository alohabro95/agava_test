<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

const props = defineProps({
  option: {
    type: Object,
    required: true,
  },
});

const isHover = ref(false);

const showTooltip = () => {
  isHover.value = true;
};

const hideTooltip = () => {
  isHover.value = false;
};
</script>

<template>
  <li class="menu__item" @mouseover="showTooltip" @mouseleave="hideTooltip">
    <img :src="option.img" alt="" />
    <div v-if="isHover" class="tooltip">
      <div class="tooltip-arrow"></div>
      <div class="tooltip-text">{{ option.tooltipText }}</div>
    </div>
  </li>
</template>
<style>
.menu__item {
  padding: 2px 0px;
  cursor: pointer;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
  background: linear-gradient(
    233.07deg,
    rgba(183, 45, 147, 1) 23.79%,
    rgba(109, 17, 133, 1) 90.03%
  );
  &:hover {
    background: linear-gradient(266.09deg, #ff4bd1 1.73%, #bb4ed8 103.36%);
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
@media screen and (min-width: 600px) {
  .menu__item {
    padding: 9px 6px;
  }
}
</style>
