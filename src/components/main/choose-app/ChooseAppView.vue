<template>
  <section class="choose-app-wrapper">
    <choose-app-title class="container" />
    <div class="desktop-grid container">
      <feature-item
        v-for="reason in reasons"
        :key="reason.title"
        :feature="reason"
        :column="true"
        :textCenter="true"
      />
    </div>
  </section>
</template>

<script setup lang="ts">
import ChooseAppTitle from "./ChooseAppTitle.vue";
import FeatureItem from "../../common/FeatureItem.vue";
import { onBeforeUnmount, onMounted, ref } from "vue";

const reasons = [
  {
    img: require("../../../styles/images/app-development.svg"),
    color: "#FFECEF",
    title: "App Development",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/award.svg"),
    color: "#EAF9FF",
    title: "10 Times Award",
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
    img: require("../../../styles/images/customization.svg"),
    color: "#E4FFEE",
    title: "Customization",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/ux-planning.svg"),
    color: "#F4F4FF",
    title: "UX Planning",
    subTitle:
      "Get your blood tests delivered at home collect a sample from the news your blood tests.",
  },
  {
    img: require("../../../styles/images/customer-support.svg"),
    color: "#FDEEE4",
    title: "Customer Support",
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
