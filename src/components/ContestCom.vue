<template>
  <section>
    <div class="contest">
      <h2 class="contest__title h2">Конкурсы сегодняшнего дня</h2>
      <div
        v-for="(item, index) in faqItems"
        :key="index"
        class="contest-container"
      >
        <div class="content__list">
          <div class="contest__item">
            <div class="contest__item-wraper">
              <p class="contest__item-subtitle p1">{{ item.subtitle }}</p>
              <p class="contest__item-publication p2">{{ item.publication }}</p>
            </div>
            <button
              @click="toggleContent(index)"
              :class="{
                'solaris__item-btn--current': isButtonActive === index,
              }"
              class="contest__item-btn"
            >
              <i 
              :class="{ 'arrow-right--current': isButtonActive === index }"
              class="arrow-right"></i>
            </button>
          </div>
          </div>
        <div 
        :class="{ 'solaris-faq-content--current': isContentActive === index }"
        class="contest-content">
          <h3 class="contest-content__title h3">Название конкурса</h3>
          <div class="contest-content__subtitle">
            <p class="contest-content__subtitle-text p2">Направление</p>
            <p class="contest-content__subtitle-start p2">начало 01.05.2024</p>
          </div>
          <p class="contest-content__description p2">
            Идейные соображения высшего порядка, а также постоянный
            количественный рост
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const isButtonActive = ref(false);
const isContentActive = ref(false);
const faqItems = ref([
  {
    subtitle: "Название конкурса",
    publication:
      "Дата публикации ",
  },
  {
    subtitle: "Название конкурса",
    publication:
      "Дата публикации ",
  },
  {
    subtitle: "Название конкурса",
    publication:
      "Дата публикации ",
  },
  {
    subtitle: "Название конкурса",
    publication:
      "Дата публикации ",
  },
  
 
  
]);

function toggleContent(index) {
  isButtonActive.value = index;

  if (isContentActive === index) {
    isContentActive.value = null;
  } else {
    isContentActive.value = index;
  }
}
</script>

<style>

.solaris-faq-content--current{
    display: flex;
    flex-direction: column;
}

.contest {
  max-width: 1440px;
  padding: 80px 60px;

  margin: auto;
  box-sizing: border-box;
}

.contest__title {
  color: var(--dark);
}

.contest-container {
  margin-top: 48px;
  display: flex;
  justify-content: space-between;
  gap: 20px;
}

.content__list {
  display: flex;
  flex-direction: column;
  max-width: 589px;
  width: 100%;
  gap: 30px;
}

.contest__item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: var(--dark);
}

.contest__item-subtitle {
  margin-right: 20px;
  min-width: 225px;
}

.contest__item-publication {
  margin-right: 25px;
}

.contest__item-btn {
  width: 24px;
  height: 24px;
  border-radius: 100%;
  border: 1px solid var(--dark);
  background: var(--white);
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.arrow-right {
  border: solid var(--dark);
  border-width: 0 1.5px 1.5px 0;
  padding: 3px;
  display: inline-block;
  transform: rotate(-45deg);
  -webkit-transform: rotate(-45deg);
  position: relative;
  left: -1px;
}

.contest-content {
  max-width: 653px;
  height: fit-content;
  border: 2px solid var(--roseBege);
  background: var(--lightBege);
  display: none;
}

.contest-content__title {
  color: var(--white);
  padding: 16px;
  background: var(--roseBege);
}

.contest-content__subtitle {
  display: flex;
  gap: 16px;
  padding: 16px;
}
.contest-content__subtitle-text,
.contest-content__subtitle-start {
  background: var(--roseBege);
  color: var(--white);
  padding: 8px;
}

.contest-content__description {
  padding: 16px;
  color: var(--dark);
}
</style>
