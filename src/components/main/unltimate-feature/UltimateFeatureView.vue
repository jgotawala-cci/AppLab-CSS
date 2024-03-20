<template>
  <section class="ultimate-feature-container">
    <div class="ultimate-feature-wrapper">
      <ultimate-feature-top />
      <ultimate-feature-middle class="mobile-view" />
      <ultimate-feature-bottom />
    </div>
    <!-- <ultimate-feature-middle class="desktop-view" /> -->
  </section>
</template>

<script setup lang="ts">
import UltimateFeatureTop from "./UltimateFeatureTop.vue";
import UltimateFeatureMiddle from "./UltimateFeatureMiddle.vue";
import UltimateFeatureBottom from "./UltimateFeatureBottom.vue";
</script>
