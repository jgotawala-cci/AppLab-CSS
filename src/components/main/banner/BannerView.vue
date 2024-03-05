<template>
  <div class="banner-container">
    <section class="banner-left">
      <banner-left-top />
      <banner-left-middle />
    </section>
    <section class="banner-right">
      <banner-right />
    </section>
    <img
      class="building-bg"
      src="../../../styles/images/building-backgorund.svg"
    />
    <img class="cross-bg" src="../../../styles/images/cross-background.svg" />
    <div class="circle-bg-container">
      <img
        class="circle-bg"
        src="../../../styles/images/circle-background.svg"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import BannerLeftTop from "./BannerLeftTop.vue";
import BannerLeftMiddle from "./BannerLeftMiddle.vue";
import BannerRight from "./BannerRight.vue";
</script>
