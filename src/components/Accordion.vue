<script setup>
import { Collapse } from "vue-collapsed";
import { reactive } from "vue";

// Пример фейковых данных
const fakeData = [
  { title: "LOREM IPSUM", answer: "Answer 1" },
  { title: "INTERDUM", answer: "Answer 2" },
  { title: "CRAS PORTA", answer: "Answer 3" },
  { title: "DIUS SEMPER", answer: "Answer 3" },
  { title: "CRASDIGNISSIM", answer: "Answer 3" },
  { title: "LOREM IPSUM DOLOR", answer: "Answer 3" },
  { title: "DUIS MINAR", answer: "Answer 3" },
  { title: "DONEC NUNC", answer: "Answer 3" },
  { title: "NULLA FACILISI", answer: "Answer 3" },
  { title: "VIVAMUS ORNARE", answer: "Answer 3" },
];

const questions = reactive(
  fakeData.map(({ title, answer }, index) => ({
    title,
    answer,
  }))
);

function handleAccordion(selectedIndex) {
  questions.forEach((_, index) => {
    questions[index].isExpanded =
      index === selectedIndex ? !questions[index].isExpanded : false;
  });
}
</script>

<template>
  <article class="Wrapper">
    <div
      v-for="(question, index) in questions"
      :key="question.title"
      class="Section"
    >
      <button
        :class="['Panel', { Active: question.isExpanded }]"
        @click="handleAccordion(index)"
      >
        {{ question.title }}
        <img
          class="arrow"
          src="../assets/images/mobile_images/accordion-arrow.png"
          alt=""
          :class="{ rotated: question.isExpanded }"
        />
      </button>

      <Collapse as="section" :when="question.isExpanded">
        <p class="CollapseContent">{{ question.answer }}</p>
      </Collapse>
    </div>
  </article>
</template>

<style scoped>
.Section {
  border-bottom: 1px #6d1185 solid;
}
.Wrapper {
  width: 100%;
}
.Panel,
.CollapseContent {
  padding: 18px 15px;
  font-family: "Ubuntu", sans-serif;
  font-size: 15px;
}
.Panel {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #3c004c;
  width: 100%;
  text-align: left;
  cursor: pointer;
  border: none;
  border-bottom: 1px #d0d0d0;
}

.arrow {
  transition: transform 0.3s ease;
}

.arrow.rotated {
  transform: rotate(180deg);
}

.CollapseContent {
  margin-top: 5px;
}
</style>
