<template>
  <li>
    <button @click="$emit('remove',todo.id)">X</button>
    {{todo.text}}
  </li>
</template>
<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true
    }
  }
};
</script>
<style scoped>
li {
  padding-left: 5px;
  color: white;
  display: block;
  font-size: 16px;
  line-height: 30px;
  list-style: none;
  height: 30px;
  /* border-bottom: 1px solid #00c185; */
  background: rgba(0, 0, 0, 0.5);
  margin-top: 5px;
}
</style>