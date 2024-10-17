<script setup>
import MenuOption from "./MenuOption.vue";
const props = defineProps({
  options: {
    type: Array,
    required: true,
  },
});
</script>
<template>
  <ul class="menu">
    <MenuOption v-for="option in props.options" :option="option" />
  </ul>
</template>
<style>
.menu {
  display: flex;
  flex-direction: column;
  gap: 3px;
  list-style: none;
  padding: 0;
  margin: 0;
}
</style>
