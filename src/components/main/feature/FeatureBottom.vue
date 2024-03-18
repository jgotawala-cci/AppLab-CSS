<template>
  <div class="figure-bottom-wrapper">
    <feature-item
      v-for="feature in features"
      :key="feature.title"
      :feature="feature"
      :isSmall="true"
      :addMargin="true"
    />
  </div>
</template>

<script setup lang="ts">
import FeatureItem from "../../common/FeatureItem.vue";

const features = [
  {
    img: require("../../../styles/images/meter.svg"),
    color: "#F5576721",
    fontColor: "#F55767",
    title: "Fast Performance",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/prototype.svg"),
    color: "#2563FF21",
    fontColor: "#2563FF",
    title: "Prototyping",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/edit-pen.svg"),
    color: "#40975F21",
    fontColor: "#40975F",
    title: "Vector Editing",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
];
</script>
