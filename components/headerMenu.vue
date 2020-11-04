<template>
  <nav class="header__menu">
    <nuxt-link
      v-for="(item, index) in menu"
      :key="index"
      :to="item.url"
      class="header__menu-link"
      >{{ item.text }}</nuxt-link
    >
    <Button
      class="header__btn"
      @btn-click="callMe"
      @hover="changeBtnText(1)"
      @mouseOut="changeBtnText(0)"
      :btnText="btnText"
    />
  </nav>
</template>

<script>
import Button from '@/components/ui/roundButton'
export default {
  components: {
    Button,
  },
  methods: {
    callMe() {
      alert('Пользователь хочет, чтобы ему позвонили')
    },
    changeBtnText(text) {
      if (text) {
        this.btnText = 'заказать звонок'
      } else {
        this.btnText = '8 800 500 65 61'
      }
    },
  },
  data() {
    return {
      btnText: '8 800 500 65 61',

      menu: [
        { url: '/', text: 'Правила' },
        { url: '/', text: 'Руководство' },
        { url: '/', text: 'О компании' },
        { url: '/', text: 'Наши услуги' },
        { url: '/', text: 'Портал' },
      ],
    }
  },
}
</script>

<style scoped>
.header__menu {
  display: flex;
  flex-direction: row;
  height: 100%;
}
.header__menu-link {
  text-decoration: none;
  margin-right: 20px;
  color: #00527b;
  height: 100%;
  display: flex;
  align-items: center;
}
.header__menu-link:hover {
  border-bottom: 2px solid #00527b;
  margin-top: 1px;
}
.header__btn {
  border: 2px solid #00527b;
  color: #00527b;
}
.header__btn:hover {
  background: linear-gradient(90deg, #d81f4f, #0268b9);
  color: #ffffff;
  border: none;
  font-size: 18px;
}
</style>
