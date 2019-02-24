<template>
  <input type="text" class="input" :value="value" v-on="listeners">
</template>
<script>
export default {
  props: {
    value: {
      type: String,
      default: ""
    }
  },
  computed: {
    listeners() {
      return {
        ...this.$listeners,
        input: e => this.$emit("input", e.target.value)
      };
    }
  }
};
</script>
<style scoped>
input {
  width: 100%;
  padding: 8px 10px;
  border: 2px solid #32485F;
}
</style>