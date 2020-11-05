<template>
  <section class="list">
    <content-wrapper class="list__wrapper">
      <img :src="imgSrc" :alt="title" class="list__img" />
      <div class="list__center-cont">
        <List :title="title" :array="array" :btnText="btnText" />
      </div>
    </content-wrapper>
  </section>
</template>

<script>
import Content from '@/components/content'
import SignUpBtn from '@/components/ui/signUpBtn'
import List from '@/components/textList'
export default {
  props: {
    title: String,
    array: Array,
    btnText: String,
    imgSrc: String,
  },
  components: {
    'content-wrapper': Content,

    List,
  },
}
</script>

<style scoped>
.list {
}
.list__center-cont {
  display: flex;
  align-items: center;
}
.list__wrapper {
  display: flex;
  flex-direction: row;
}

.list__img {
  height: 676px;
  margin: 0 44px;
}
</style>
