<template>
  <div class="tab-item">
    <div
      class="tab-item__title"
      :style="{
        backgroundColor: '#f00',
        padding: '4px',
        cursor: 'pointer',
        width: '70px'
      }"
      @click="$emit('onChangeTab', props.tabKey)"
    >{{ props.title }}</div>
    <div v-if="isActive" class="tab-item__content">
      <slot />
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  tabKey: {
    type: String,
    required: true,
  },
  isActive: {
    type: Boolean,
    default: false,
  }
});

</script>