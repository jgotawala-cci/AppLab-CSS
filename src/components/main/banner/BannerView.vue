<template>
  <section id="home" class="banner-container">
    <div class="container element-container">
      <banner-left-middle />
      <banner-right />
      <span class="circle-gredient-out element element-1">
        <span class="circle-gredient-in"></span>
      </span>
      <span class="plus-blue element element-2"></span>
      <span class="desktop-view circle-gredient-out element element-3">
        <span class="circle-gredient-in"></span>
      </span>
      <span class="desktop-view circle-gredient-out element element-4">
        <span class="circle-gredient-in"></span>
      </span>
      <span class="desktop-view circle-purple element element-5"></span>
      <span class="desktop-view squre-purple element element-6"></span>
      <span class="desktop-view cross-purple element element-7"></span>
      <span class="desktop-view cross-purple element element-8"></span>
    </div>
    <div class="building-bg"></div>
  </section>
</template>

<script setup lang="ts">
import BannerLeftMiddle from "./BannerLeftMiddle.vue";
import BannerRight from "./BannerRight.vue";
</script>
