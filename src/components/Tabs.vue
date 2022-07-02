<template>
  <div
    :style="{
      backgroundColor: props.bgColor,
      color: props.txtColor,
      width: props.width,
      height: props.height,
    }"
  >
    <slot />
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  bgColor: {
    type: String,
    default: '#F00',
  },
  txtColor: {
    type: String,
    default: 'yellow',
  },
  width: {
    type: String,
    default: '990px',
  },
  height: {
    type: String,
    default: '500px'
  }
});

</script>

<style></style>