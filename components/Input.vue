<template>
  <v-text-field
    v-model="localModel"
    dense
    :label="label"
    outlined
    rounded
    :rules="rules"
    :type="type"
  ></v-text-field>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: "label",
    },
    model: {
      type: String,
      default: null,
    },
    rules: {
      type: Array,
      default: () => [],
    },
    type: {
      type: String,
      default: "text",
    },
  },
  data() {
    return {
      localModel: this.model,
    };
  },
  watch: {
    localModel(val) {
      this.$emit("update:model", val);
    },
    model(val) {
      this.localModel = val;
    },
  },
};
</script>

<style></style>
