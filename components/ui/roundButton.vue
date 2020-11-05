<template>
  <button
    @click="$emit('btn-click')"
    @mouseover="$emit('hover')"
    @mouseout="$emit('mouseOut')"
    class="button"
  >
    {{ btnText }}
  </button>
</template>

<script>
export default {
  props: ['btnText'],
}
</script>

<style scoped>
.button {
  font-size: 20px;
  height: 44px;
  min-width: 190px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  font-weight: bold;
  border-radius: 50px;
  cursor: pointer;
  text-transform: uppercase;
  outline: none;
}
</style>
