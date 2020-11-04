<template>
  <header class="header">
    <content-wrapper class="header__content">
      <div class="header__container">
        <nuxt-link to="/" class="header__logo"></nuxt-link>
        <span class="header__logo-separator">/</span>
        <p @click="services" class="header__services">Моя квартира</p>
        <button @click="services" class="header__services-btn"></button>
      </div>
      <div class="header__container">
        <header-menu />
      </div>
    </content-wrapper>
  </header>
</template>

<script>
import Content from '@/components/content'
import Menu from '@/components/headerMenu'
export default {
  components: {
    'content-wrapper': Content,
    'header-menu': Menu,
  },
  methods: {
    services() {
      alert('Пользователь открыл модальное окно "Услуги"')
    },
  },
}
</script>

<style scoped>
.header {
  width: 100%;
  background-color: transparent;
  padding: 18px 0;
}
.header__content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.header__container {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding-bottom: 12px;
}
.header__logo {
  background-image: url('https://roskvartal-a.akamaihd.net/Dispatch/Landing/rk-logo.svg');
  background-repeat: no-repeat;
  width: 202px;
  height: 40px;
  cursor: pointer;
  position: relative;
  bottom: 5px;
}
.header__logo-separator {
  font-size: 32px;
  margin-right: 20px;
  margin-left: 8px;
  font-weight: 200;
}
.header__services {
  color: #131313;
  font-size: 24px;
  cursor: pointer;
  height: 100%;
  display: flex;
  align-items: center;
}
.header__services:hover {
  border-bottom: 1px dotted #131313;
  margin-top: 1px;
}
.header__services-btn {
  width: 32px;
  height: 32px;
  border: none;
  background-color: transparent;
  background-image: url('../static/services.svg');
  background-repeat: no-repeat;
  position: relative;
  top: 10px;
  margin-left: 12px;
  cursor: pointer;
  outline: none;
}
</style>
