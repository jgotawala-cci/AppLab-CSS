<template>
  <section class="main-header container">
    <img src="../../styles/images/app-lab-icon.svg" />
    <a href="#"
      ><img @click="onShowOverlay" :src="menu_img" :class="{ active: isOpen }"
    /></a>
    <header-slider
      :overlayStyle="overlayStyle"
      :onCloseOverlay="onCloseOverlay"
    ></header-slider>
  </section>
  <section class="desktop-header">
    <nav>
      <a href="#">Home</a>
      <a href="#">Key Features</a>
      <a href="#">Pricing</a>
      <a href="#">Testimonial</a>
      <a href="#">FAQ</a>
    </nav>
    <button>Try for free</button>
  </section>
</template>

<script setup lang="ts">
import HeaderSlider from "./HeaderSlider.vue";

import { onBeforeUnmount, onMounted, ref, watch } from "vue";

const isMobile = ref(window.innerWidth <= 768); // Adjust the threshold as needed
const isOpen = ref(false);
const menu_img = ref(require("../../styles/images/menu.svg"));
const overlayStyle = ref({ right: "-100%" });

const handleResize = () => {
  isMobile.value = window.innerWidth <= 768; // Adjust the threshold as needed
};

const onShowOverlay = () => {
  if (isMobile.value) {
    if (isOpen.value) {
      onCloseOverlay();
      return;
    }
    overlayStyle.value = { right: "0%" };
    document.body.classList.add("no-scroll");
    isOpen.value = true;
    menu_img.value = require("../../styles/images/cross.svg");
  }
};

const onCloseOverlay = () => {
  overlayStyle.value = { right: "-100%" };
  document.body.classList.remove("no-scroll");
  isOpen.value = false;
  menu_img.value = require("../../styles/images/menu.svg");
};

onMounted(() => {
  window.addEventListener("resize", handleResize);
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", handleResize);
});

watch(isMobile, () => {
  if (isOpen.value) {
    onCloseOverlay();
  }
});
</script>
