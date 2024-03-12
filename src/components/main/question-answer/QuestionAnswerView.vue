<template>
  <section @click="onExpand(-1)">
    <question-answer-title />
    <expandable-view
      v-for="questionAnswer in questionAnswers"
      :key="questionAnswer.no"
      :questionAnswer="questionAnswer"
      :onExpand="onExpand"
      :isExpanded="isExpanded(questionAnswer.no)"
    />
  </section>
</template>

<script setup lang="ts">
import QuestionAnswerTitle from "./QuestionAnswerTitle.vue";
import ExpandableView from "../../common/ExpandableView.vue";
import { ref } from "vue";

const questionAnswers = [
  {
    no: 1,
    question: "How to contact with riders emergency?",
    answer:
      "Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
  },
  {
    no: 2,
    question: "App installation failed, how to update system information?",
    answer:
      "Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
  },
  {
    no: 3,
    question: "Website response taking time, how to improve?",
    answer:
      "Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
  },
  {
    no: 4,
    question: "New update fixed all bug and issues",
    answer:
      "Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
  },
  {
    no: 5,
    question: "How to contact with riders emergency?",
    answer:
      "Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
  },
];
const currentItemValue = ref(-1);
const isExpanded = (currentItem: number) => {
  return currentItem === currentItemValue.value;
};
const onExpand = (key: number) => {
  if (currentItemValue.value === key) {
    currentItemValue.value = -1;
    return;
  }
  currentItemValue.value = key;
};
</script>
