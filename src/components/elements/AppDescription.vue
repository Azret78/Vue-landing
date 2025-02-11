<template>
  <div class="description__inner">
    <div class="description__left">
      <div class="description__logo">
        <picture>
          <img
            :src="descriptionLogo"
            title=""
            alt=""
            width="200"
            height="140"
          />
        </picture>
      </div>
      <div class="description__text">
        <p>{{ descriptionText }}</p>
      </div>
    </div>
    <div class="description__video">
      <picture>
        <img :src="descriptionPoster" alt="" title="" width="" height />
      </picture>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    descriptionLogo: String,
    descriptionText: String,
    descriptionPoster: String,
  },
};
</script>
