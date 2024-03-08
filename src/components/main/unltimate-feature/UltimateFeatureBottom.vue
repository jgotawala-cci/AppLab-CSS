<template>
  <div class="ultimate-desktop-grid">
    <feature-item
      v-for="reason in reasons"
      :key="reason.title"
      :feature="reason"
      :column="true"
      :textCenter="true"
    />
  </div>
  <button class="desktop-view">See all</button>
</template>

<script setup lang="ts">
import FeatureItem from "../../common/FeatureItem.vue";

const reasons = [
  {
    img: require("../../../styles/images/app-development.svg"),
    color: "#FFECEF",
    title: "App Development",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/ux-planning.svg"),
    color: "#E4FFEE",
    title: "UX Planning",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/cloud-storage.svg"),
    color: "#FFF6D3",
    title: "Cloud Storage",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/customer-support.svg"),
    color: "#F4F4FF",
    title: "Customer Support",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
];
</script>
