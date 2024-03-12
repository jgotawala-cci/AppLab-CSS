<template>
  <div id="key-feature" class="feature-wrapper">
    <feature-top class="mobile-view" />
    <feature-middle />
    <div>
      <feature-top class="desktop-view" />
      <feature-bottom />
    </div>
  </div>
</template>

<script setup lang="ts">
import FeatureTop from "./FeatureTop.vue";
import FeatureMiddle from "./FeatureMiddle.vue";
import FeatureBottom from "./FeatureBottom.vue";
</script>
