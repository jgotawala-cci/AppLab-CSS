<template>
  <aside class="overlay" :style="props.overlayStyle">
    <nav>
      <a href="#home" @click="props.onCloseOverlay">Home</a>
      <a href="#key-feature" @click="props.onCloseOverlay">Key Features</a>
      <a href="#pricing" @click="props.onCloseOverlay">Pricing</a>
      <a href="#testimonial" @click="props.onCloseOverlay">Testimonial</a>
      <a href="#faq" @click="props.onCloseOverlay">FAQ</a>
    </nav>
    <button @click="props.onCloseOverlay">Try for free</button>
  </aside>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps(["overlayStyle", "onCloseOverlay"]);
</script>
