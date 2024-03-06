<template>
  <section class="benifits-wrapper">
    <benifit-title />
    <div class="desktop-grid">
      <feature-item
        v-for="benifit in benifits"
        :key="benifit.title"
        :feature="benifit"
        :column="true"
        :textCenter="true"
        :textLeft="!isMobile"
      />
    </div>
  </section>
</template>

<script setup lang="ts">
import BenifitTitle from "./BenifitTitle.vue";
import FeatureItem from "../../common/FeatureItem.vue";
import { onBeforeUnmount, onMounted, ref } from "vue";

const benifits = [
  {
    img: require("../../../styles/images/payouts.svg"),
    color: "#F5576721",
    fontColor: "#F55767",
    title: "Automatic Payouts",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/network.svg"),
    color: "#2563FF21",
    fontColor: "#2563FF",
    title: "Network Effect",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/reward.svg"),
    color: "#40975F21",
    fontColor: "#40975F",
    title: "Bigger Rewards Method",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
];

const isMobile = ref(window.innerWidth <= 768);
const handleResize = () => {
  isMobile.value = window.innerWidth <= 768; // Adjust the threshold as needed
};
onMounted(() => {
  window.addEventListener("resize", handleResize);
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", handleResize);
});
</script>
