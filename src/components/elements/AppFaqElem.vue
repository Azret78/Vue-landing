<template>
  <div class="faq__elem" :class="isActive ? '_active' : ''">
    <div class="faq__top" @click="toggleActive">
      <div class="faq__subtitle">
        <h3>{{ faqTitle }}</h3>
      </div>
      <div class="faq__arrow">
        <svg
          width="30"
          height="17"
          viewBox="0 0 30 17"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M1 1.70605L15 15.7061L29 1.70605"
            stroke="#2F2F51"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </div>
    </div>
    <div class="faq__subtext">
      <p>{{ faqText }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    faqTitle: String,
    faqText: String,
  },
  emits: ["openFaq"],
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    toggleActive() {
      this.isActive = !this.isActive;
    },
  },
};
</script>
