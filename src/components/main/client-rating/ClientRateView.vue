<template>
  <div id="testimonial" class="client-rating-divider">
    <section class="client-rating-container">
      <h3 class="mobile-view">Meet Client Satisfaction by using product</h3>
      <figure class="mobile-view">
        <img
          src="../../../styles/images/peoples.svg"
          width="526"
          height="400"
        />
      </figure>
      <client-pager />
    </section>
  </div>
</template>

<script setup lang="ts">
import ClientPager from "./ClientPager.vue";
</script>
