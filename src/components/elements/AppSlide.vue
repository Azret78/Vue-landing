<template>
  <div class="feedback__slide">
    <div class="feedback__top">
      <div class="feedback__name">
        <p>{{ slideItem.name }}</p>
      </div>
      <div class="feedback__date">
        <p>{{ slideItem.date }}</p>
      </div>
      <div class="feedback__dogovor">
        <p>Договор № {{ slideItem.dogovor }}</p>
      </div>
    </div>
    <div class="feedback__text">
      <p>{{ slideItem.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    slideItem: {
      type: Object,
      default: () => {},
    },
  },
};
</script>
