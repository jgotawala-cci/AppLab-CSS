<template>
  <section class="main-header container">
    <img src="../../styles/images/app-lab-icon.svg" width="118" height="44" />
    <div class="menu-icon" :class="{ open: isOpen }" @click="onShowOverlay">
      <span class="line"></span>
      <span class="line"></span>
      <span class="line"></span>
    </div>
    <header-slider
      :overlayStyle="overlayStyle"
      :onCloseOverlay="onCloseOverlay"
    ></header-slider>
  </section>
  <section class="desktop-header container">
    <nav>
      <a href="#home">Home</a>
      <a href="#key-feature">Key Features</a>
      <a href="#pricing">Pricing</a>
      <a href="#testimonial">Testimonial</a>
      <a href="#faq">FAQ</a>
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
