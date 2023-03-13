<template>
  <div class="tooltip-container" @click="toggleTooltip">
    <slot></slot>
    <div v-if="tooltipVisible" class="tooltip">
      <NuxtLink>App Store</NuxtLink>
      <NuxtLink>Google Play</NuxtLink>
    </div>
  </div>
</template>

<script>
import {ref, onMounted} from 'vue';

export default {
  name: 'Tooltip',

  setup() {
    const tooltipVisible = ref(false);

    function toggleTooltip() {
      tooltipVisible.value = !tooltipVisible.value;
    }

    onMounted(() => {
      window.addEventListener('click', handleClickOutside);
    });

    function handleClickOutside(event) {
      if (!event.target.closest('.tooltip-container')) {
        tooltipVisible.value = false;
      }
    }

    return {
      tooltipVisible,
      toggleTooltip
    };
  }
};
</script>

<style>
.tooltip-container {
  position: relative;
  display: inline-block;
}

.tooltip {
  margin-top: 11px;
  position: absolute;
  width: 100%;
  display: flex;
  flex-direction: column;
  top: 100%;
  left: 50%;
  line-height: 28px;
  font-weight: 400;
  font-size: 14px;
  transform: translateX(-50%);
  padding: 7px 12px;
  background: #FFFFFF;
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  color: #23153E;
  z-index: 1;
}

.tooltip::after {
  content: '';
  position: absolute;
  top: -0.25rem;
  left: 50%;
  transform: translateX(-50%);
  background: #FFFFFF;
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
}
</style>
