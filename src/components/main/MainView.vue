<template>
  <banner-view />
  <company-view />
  <feature-view class="container" />
  <benifits-view class="container" />
  <design-info-view class="container" />
  <choose-app-view />
  <ultimate-feature-view class="container" />
  <price-view class="container center" />
</template>

<script setup lang="ts">
import BannerView from "./banner/BannerView.vue";
import CompanyView from "./companies/CompanyView.vue";
import FeatureView from "./feature/FeatureView.vue";
import BenifitsView from "./benifits/BenifitsView.vue";
import DesignInfoView from "./design-info/DesignInfoView.vue";
import ChooseAppView from "./choose-app/ChooseAppView.vue";
import UltimateFeatureView from "./unltimate-feature/UltimateFeatureView.vue";
import PriceView from "./pricing/PriceView.vue";
</script>
