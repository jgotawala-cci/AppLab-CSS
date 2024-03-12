<template>
  <section class="page-container">
    <profile-view class="mobile-view" />
    <h2 class="desktop-view">Meet Client Satisfaction by using product</h2>
    <p>
      The rise of mobile devices transforms the way we consume, elegant channels
      such as Facebook.
    </p>

    <div class="rating-container desktop-view">
      <img src="../../../styles/images/star.svg" />
      <img src="../../../styles/images/star.svg" />
      <img src="../../../styles/images/star.svg" />
      <img src="../../../styles/images/star.svg" />
      <img src="../../../styles/images/star.svg" />
    </div>
    <h5>User friendly & Customizable</h5>
    <p>
      Bring to the table win-win survival strategies to ensure proactive
      domination. At the end of the day, going forward, a new normal that has
      evolved from generation X is on the runway heading towards a streamlined
      cloud solution. User generated content in real-time will have multiple
      touchpoints for offshoring.
    </p>
    <div class="profile-data desktop-view">
      <img
        class="profile-image"
        src="../../../styles/images/profile-image.svg"
      />
      <div class="name-designation">
        <h5>Zoltan Nemeth</h5>
        <span>CEO of Pixler Lab</span>
      </div>
      <div class="pagination-wrapper">
        <img
          class="prev disable"
          src="../../../styles/images/disable-arrow.svg"
        />
        <div class="divider"></div>
        <img class="next" src="../../../styles/images/active-arrow.svg" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import ProfileView from "../../common/ProfileView.vue";
</script>
