<template>
  <h2 class="section-title">{{ title }}</h2>
</template>

<script>
export default {
  props: ['title'],
}
</script>

<style scoped>
.section-title {
  font-size: 34px;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
}
</style>
