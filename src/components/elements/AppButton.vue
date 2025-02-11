<template>
  <a :href="href" :class="classType"><slot></slot></a>
</template>

<script>
export default {
  props: {
    classType: String,
    href: String,
  },
};
</script>

<style lang="scss" scoped></style>
