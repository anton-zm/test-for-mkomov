<template>
  <a class="share-btn" :href="link">
    <img :src="img" :alt="source" class="share-btn__icon" />
    <p class="share-btn__text">{{ source }}</p>
  </a>
</template>

<script>
export default {
  props: ['link', 'img', 'source'],
}
</script>

<style scoped>
.share-btn {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.share-btn__icon {
  width: 14px;
  height: 16px;
}
.share-btn__text {
}
</style>
