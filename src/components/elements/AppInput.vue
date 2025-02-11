<template>
  <input
    :type="type"
    :placeholder="placeholder"
    :value="value"
    @input="change"
  />
  <small v-if="error">{{ error }}</small>
</template>

<script>
export default {
  props: {
    placeholder: String,
    type: String,
    error: String,
    value: {
      type: [String, Number],
    },
  },
  methods: {
    change(event) {
      this.$emit("update:value", event.target.value);
    },
  },
};
</script>
