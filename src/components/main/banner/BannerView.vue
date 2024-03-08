<template>
  <div class="banner-container">
    <div class="container">
      <section class="banner-left">
        <banner-left-top />
        <banner-left-middle />
      </section>
      <section class="banner-right">
        <banner-right />
      </section>
    </div>
    <img
      class="cross-bg desktop-view"
      src="../../../styles/images/cross-background.svg"
    />
    <div class="building-bg"></div>
    <img class="circle-bg" src="../../../styles/images/circle-background.svg" />
  </div>
</template>

<script setup lang="ts">
import BannerLeftTop from "./BannerLeftTop.vue";
import BannerLeftMiddle from "./BannerLeftMiddle.vue";
import BannerRight from "./BannerRight.vue";
</script>
