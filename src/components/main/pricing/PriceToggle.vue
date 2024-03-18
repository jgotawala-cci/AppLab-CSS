<template>
  <div class="toggle">
    <label
      for="monthly"
      class="toggle-text"
      :class="{ 'active-label': isMonthly, 'inactive-lable': !isMonthly }"
      @click="onMonthly"
      >Monthly</label
    >
    <div class="toggle-button mobile-view" @click="onToggle">
      <div class="toggle-circle" :class="{ right: !isMonthly }"></div>
    </div>
    <label
      for="annually"
      class="toggle-text"
      :class="{ 'active-label': !isMonthly, 'inactive-lable': isMonthly }"
      @click="onAnnually"
      >Annually</label
    >
  </div>
</template>

<script setup lang="ts">
import { inject, ref } from "vue";

const isMonthly = inject("isMonthly", ref(true));

const onToggle = () => {
  isMonthly.value = !isMonthly.value;
};

const onMonthly = () => {
  isMonthly.value = true;
};
const onAnnually = () => {
  isMonthly.value = false;
};
</script>
