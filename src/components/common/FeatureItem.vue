<template>
  <div
    class="feature-item"
    :class="{
      'is-small': props.isSmall,
      column: props.column,
      'text-center': props.textCenter,
      'text-left': props.textLeft,
    }"
  >
    <figure :style="img_background" :class="{ 'is-small': props.isSmall }">
      <img
        :src="props.feature.img"
        :class="{ 'is-small': props.isSmall }"
        width="88"
        height="88"
      />
    </figure>
    <figcaption :class="{ 'add-margin': props.addMargin }">
      <h4 :class="{ 'is-small': props.isSmall }" :style="font_color">
        {{ props.feature.title }}
      </h4>
      <p :class="{ 'is-small': props.isSmall }">
        {{ props.feature.subTitle }}
      </p>
    </figcaption>
  </div>
</template>

<script setup lang="ts">
import { defineProps, ref } from "vue";

const props = defineProps([
  "feature",
  "isSmall",
  "addMargin",
  "centerAlign",
  "column",
  "textCenter",
  "textLeft",
]);
const img_background = ref({ "background-color": props.feature.color });
const font_color = ref({ color: props.feature.fontColor });
</script>
