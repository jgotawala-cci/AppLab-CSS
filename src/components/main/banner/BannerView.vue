<template>
  <div id="home" class="banner-container">
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
      width="504px"
      height="403px"
      src="../../../styles/images/cross-background.svg"
    />
    <div class="building-bg"></div>
    <img
      class="circle-bg"
      width="806px"
      height="605px"
      src="../../../styles/images/circle-background.svg"
    />
  </div>
</template>

<script setup lang="ts">
import BannerLeftTop from "./BannerLeftTop.vue";
import BannerLeftMiddle from "./BannerLeftMiddle.vue";
import BannerRight from "./BannerRight.vue";
</script>
