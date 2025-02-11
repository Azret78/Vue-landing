<template>
  <div class="work__inner">
    <div class="work__title">
      <h2>{{ title }}</h2>
    </div>
    <div class="work__body">
      <div class="work__elem" v-for="elem in elems" :key="elem">
        <div class="work__img">
          <picture>
            <img
              :src="elem.workImage"
              alt=""
              title=""
              width="100"
              height="83"
            />
          </picture>
        </div>
        <div class="work__subtitle">
          <h3>{{ elem.workTitle }}</h3>
        </div>
        <div class="work__subtext">
          <p>{{ elem.workText }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    elems: Array,
  },
};
</script>
