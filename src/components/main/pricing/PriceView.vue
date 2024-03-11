<template>
  <section>
    <price-title />
    <price-toggle />
    <card-view />
  </section>
</template>
<script setup lang="ts">
import PriceTitle from "./PriceTitle.vue";
import PriceToggle from "./PriceToggle.vue";
import CardView from "./CardView.vue";
import { provide, ref } from "vue";

const isMonthly = ref(true);
provide("isMonthly", isMonthly);
</script>
