<template>
  <v-img :max-height="maxHeight" :max-width="maxWidth" :src="src"></v-img>
</template>

<script>
export default {
  props: {
    maxHeight: {
      type: String,
      default: "150",
    },
    maxWidth: {
      type: String,
      default: "250",
    },
    src: {
      type: String,
      default: null,
    },
  },
};
</script>
