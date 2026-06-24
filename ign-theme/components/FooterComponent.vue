<template>
  <footer class="mon-header">
    <p>{{ author }}</p>
    <p>{{ page }} / {{ total }}</p>
    <p>{{ title }}</p>
  </footer>
</template>

<script setup lang="ts">
const props = defineProps({
  author: {
    type: String,
    default: "really, nobody authored this?",
  },
  title: {
    type: String,
    default: "no titles defined",
  },
  total: {
    type: Number,
    default: "0",
  },page: {
    type: Number,
    default: "0",
  },
})
</script>

<style scoped>
.mon-header {
  background-color: white;
  color: #787878;
  font-size: 0.7em;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 30px;
  padding: 0 1rem;
}
</style>