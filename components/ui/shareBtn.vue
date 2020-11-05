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
  justify-content: center;
  transition: transform 0.1s ease-in-out;
  border: 1px solid #d4d8de;
  box-sizing: border-box;
  border-radius: 4px;
  padding: 10px 20px;
  margin-right: 12px;
  text-decoration: none;
}
.share-btn__icon {
  width: 14px;
  height: 16px;
}
.share-btn__text {
  letter-spacing: 1px;
  font-size: 13px;
  line-height: 16px;
  font-weight: bold;
  text-transform: uppercase;
  color: #262626;
  margin-left: 12px;
}
.share-btn:hover {
  transform: translateY(-5px);
}
</style>
