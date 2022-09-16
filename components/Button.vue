<template>
  <v-btn
    v-text="label"
    :color="color"
    :dark="!disabled"
    :disabled="disabled"
    rounded
    :type="type"
  />
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "primary",
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    label: {
      type: String,
      default: "label",
    },
    type: {
      type: String,
      default: "button",
    },
  },
};
</script>

<style></style>
