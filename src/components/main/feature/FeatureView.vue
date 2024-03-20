<template>
  <section id="key-feature" class="feature-wrapper">
    <feature-top class="mobile-view" />
    <feature-middle class="mobile-view" />
    <div class="feature-content">
      <feature-top class="desktop-view" />
      <feature-bottom />
    </div>
  </section>
</template>

<script setup lang="ts">
import FeatureTop from "./FeatureTop.vue";
import FeatureMiddle from "./FeatureMiddle.vue";
import FeatureBottom from "./FeatureBottom.vue";
</script>
