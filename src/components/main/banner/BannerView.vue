<template>
  <section id="home" class="banner-container">
    <div class="container">
      <banner-left-middle />
      <banner-right />
    </div>
    <img
      class="cross-bg desktop-view"
      width="504"
      height="403"
      src="../../../styles/images/cross-background.svg"
    />
    <div class="building-bg"></div>
    <img
      class="circle-bg"
      width="806"
      height="605"
      src="../../../styles/images/circle-background.svg"
    />
  </section>
</template>

<script setup lang="ts">
import BannerLeftMiddle from "./BannerLeftMiddle.vue";
import BannerRight from "./BannerRight.vue";
</script>
