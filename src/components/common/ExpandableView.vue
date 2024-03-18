<template>
  <div class="expandable-container" :class="{ 'extra-padding': isExpanded }">
    <div class="expand-trigger">
      <h4
        :class="{
          'expand-question': isExpanded,
          'ellipsis-question': !isExpanded,
        }"
      >
        {{ props.questionAnswer.question }}
      </h4>
      <img
        width="15px"
        height="15px"
        @click.stop="props.onExpand(props.questionAnswer.no)"
        src="../../styles/images/plus-icon.svg"
        :class="{ 'hide-icon': isExpanded }"
      />
    </div>
    <div class="expand-content" :class="{ 'answer-show': isExpanded }">
      <p>
        {{ props.questionAnswer.answer }}
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps(["questionAnswer", "isExpanded", "onExpand"]);
</script>
