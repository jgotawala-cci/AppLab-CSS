<template>
  <section class="card-wrapper">
    <div class="card-view">
      <div class="card-top">
        <h1>$0</h1>
        <span>/{{ isMonthly ? "month" : "year" }}</span>
        <h4>Business Class</h4>
        <span>For small teams or office</span>
      </div>
      <div class="card-bottom">
        <span>Drag & Drop Builder </span>
        <span>1,000's of Templates</span>
        <span>Blog Support Tools</span>
        <span>eCommerce Store</span>
        <button>Start free trial</button>
      </div>
    </div>
    <div class="card-view border">
      <div class="card-top">
        <h1>${{ isMonthly ? "99" : "999" }}</h1>
        <span>/{{ isMonthly ? "month" : "year" }}</span>
        <h4>Pro Master</h4>
        <span>For Best opportunities</span>
      </div>
      <div class="card-bottom">
        <span>Drag & Drop Builder </span>
        <span>1,000's of Templates</span>
        <span>Blog Support Tools</span>
        <span>eCommerce Store</span>
        <button>Subscribe Now</button>
        <a href="#">Or Start 14 days trail</a>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { inject, ref } from "vue";

const isMonthly = inject("isMonthly", ref(true));
</script>
