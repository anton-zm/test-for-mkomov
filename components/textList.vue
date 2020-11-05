<template>
  <div class="list__content">
    <h3 class="list__title">{{ title }}</h3>
    <ul class="list__list">
      <li v-for="(item, index) in array" :key="index" class="list__item">
        {{ item }}
      </li>
    </ul>
    <SignUpBtn class="list__signup" :btnText="btnText" />
  </div>
</template>

<script>
import SignUpBtn from '@/components/ui/signUpBtn'
export default {
  props: {
    title: String,
    array: Array,
    btnText: String,
  },
  components: {
    SignUpBtn,
  },
}
</script>

<style scoped>
.list__content {
  margin-left: 32px;
}
.list__title {
  font-size: 28px;
  color: #046ab4;
  font-weight: bold;
}
.list__list {
  list-style-type: none;
  padding-left: 0;
  margin-top: 30px;
}
.list__item {
  font-size: 18px;
  line-height: 32px;
}
.list__item::before {
  content: '-';
  margin-right: 4px;
}
.list__signup {
  margin-top: 20px;
}
</style>
