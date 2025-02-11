<template>
  <div class="index__elem">
    <div class="index__img">
      <picture>
        <img :src="src" title="" alt="" width="90" height="80" />
      </picture>
    </div>
    <div class="index__text">
      <p>
        {{ text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    text: String,
    src: {
      type: String,
      required: true,
    },
  },
};
</script>
