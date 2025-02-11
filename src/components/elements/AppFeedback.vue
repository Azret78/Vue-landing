<template>
  <div class="feedback__inner">
    <app-button :class="'orange'">Оставить отзыв</app-button>
    <div class="feedback__wrapper">
      <div
        class="feedback__carusel"
        :style="{ 'margin-left': '-' + 100 * activeIndex + '%' }"
      >
        <app-slide
          :slideItem="slideItem"
          v-for="slideItem in slides"
          :key="slideItem.id"
        ></app-slide>
      </div>
      <div
        class="feedback__slide-prev"
        :class="activeIndex === 0 ? 'disable' : ''"
        @click="$emit('prev')"
      >
        <svg
          width="22"
          height="42"
          viewBox="0 0 22 42"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M21 1L1 21L21 41" stroke="black" />
          <path d="M21 1L1 21L21 41" stroke="#2F2F51" />
        </svg>
      </div>
      <div
        class="feedback__slide-next"
        :class="activeIndex === slides.length - 1 ? 'disable' : ''"
        @click="$emit('next')"
      >
        <svg
          width="22"
          height="42"
          viewBox="0 0 22 42"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M0.5 1L20.5 21L0.5 41" stroke="black" />
          <path d="M0.5 1L20.5 21L0.5 41" stroke="black" />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
import AppButton from "./AppButton.vue";
import AppSlide from "./AppSlide.vue";

export default {
  props: {
    slides: {
      type: Array,
      default: () => [],
    },
    activeIndex: Number,
  },
  emits: ["prev", "next"],
  data() {
    return {
      localFormName: this.formName,
      localFormDogovor: this.formDogovor,
      localFormText: this.formText,
    };
  },
  components: { AppButton, AppSlide },
};
</script>
