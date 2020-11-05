<template>
  <footer class="footer">
    <content-wrapper class="footer__content">
      <div class="footer__menu">
        <div class="footer__column">
          <Button
            @btn-click="lk"
            class="footer__lk-btn"
            :btnText="'личный кабинет'"
          />
          <nuxt-link to="/" class="footer__first-column-links ask"
            >Задать вопрос</nuxt-link
          >
          <nuxt-link to="/" class="footer__first-column-links"
            >Письмо директору</nuxt-link
          >
        </div>
        <div
          v-for="(column, index) in footerMenu"
          :key="index"
          class="footer__column"
        >
          <h3 class="footer__column-title">{{ column.title }}</h3>
          <ul class="footer__links-group">
            <li
              class="footer__links-list-item"
              v-for="(link, index) in column.group"
              :key="index"
            >
              <nuxt-link class="footer__link" :to="link.url">{{
                link.text
              }}</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__bottom">
        <div class="footer__bottom-container">
          <ul class="footer__socials">
            <li
              class="footer__social"
              v-for="(item, index) in socials"
              :key="index"
            >
              <a
                :href="item.url"
                :title="item.title"
                class="footer__social-icon"
                ><img
                  class="footer__social-icon-img"
                  :src="item.img"
                  :alt="item.title"
              /></a>
            </li>
          </ul>
          <div class="footer__bottom-text-wrapper mail">
            <p class="footer__bottom-text">Наша почта:</p>
            <p class="footer__bottom-text">mail@roskvartal.ru</p>
          </div>
        </div>
        <div class="footer__bottom-container">
          <div class="footer__bottom-text-wrapper callfree">
            <p class="footer__bottom-text">Бесплатный звонок</p>
            <p class="footer__bottom-text">по всей территории России</p>
          </div>
          <p class="footer__phone">8 800 500-65-61</p>
          <button @click="callMe" class="footer__bottom-btn">
            заказать звонок
          </button>
        </div>
      </div>
    </content-wrapper>
  </footer>
</template>

<script>
import Content from '@/components/content'
import Button from '@/components/ui/roundButton'

export default {
  components: {
    'content-wrapper': Content,
    Button,
  },
  data() {
    return {
      footerMenu: [
        {
          title: 'Компания',
          group: [
            { text: 'О нас', url: '/' },
            { text: 'Команда', url: '/' },
            { text: 'Часто задаваемые вопросы', url: '/' },
            { text: 'Материалы для СМИ', url: '/' },
            { text: 'Официальные документы', url: '/' },
          ],
        },
        {
          title: 'Услуги',
          group: [
            { text: 'ГИС ЖКХ', url: '/' },
            { text: 'Реформа ЖКХ', url: '/' },
            { text: 'Проведение ОСС', url: '/' },
            { text: 'Сайт для УК/ТСЖ', url: '/' },
            { text: 'Юридическая поддержка', url: '/' },
          ],
        },
        {
          title: 'ПОЛЕЗНЫЕ СЕРВИСЫ',
          group: [
            { text: 'Портал', url: '/' },
            { text: 'Сервис «ОСС на 100%»', url: '/' },
            { text: 'ЖКХ-Партнёры', url: '/' },
            { text: 'Онлайн-школа ЖКХ', url: '/' },
            { text: 'Лицензионный тест УК', url: '/' },
            { text: 'Новый вебинар для УК/ТСЖ', url: '/' },
          ],
        },
      ],
      socials: [
        {
          url: 'https://vk.com/roskvartal',
          img: 'vk.png',
          title: 'Мы во ВКонтакте',
        },
        {
          url: 'https://www.facebook.com/RosKvartal',
          img: 'facebook.png',
          title: 'Мы в Facebook',
        },
        {
          url: 'https://ok.ru/group/54946626666502',
          img: 'ok.png',
          title: 'Мы в Одноклассниках',
        },
        {
          url: 'https://www.youtube.com/channel/UC5t7A6P-Ewrug7zVyLOgUGg',
          img: 'youtube.png',
          title: 'Мы на YouTube',
        },
        {
          url: 'https://twitter.com/roskvartal',
          img: 'twitter.png',
          title: 'Мы в Twitter',
        },
        {
          url: 'https://live.viber.com/#/roskvartal',
          img: 'viber.png',
          title: 'Мы в Viber',
        },
        {
          url: 'https://t.me/roskvartal',
          img: 'telegram.png',
          title: 'Мы в Telegram',
        },
      ],
    }
  },
  methods: {
    lk() {
      alert('Пользователь ушел в личный кабинет ')
      // this.$router.push('/')
    },
    callMe() {
      alert('Пользователь хочет, чтобы ему позвонили')
    },
  },
}
</script>

<style scoped>
.footer {
  background-image: url(http://roskvartal-a.akamaihd.net/Web.Common/Images/footer-portal-back.jpg);
  background-size: cover;
  background-color: #00527b;
  padding: 36px 0;
}

.footer__menu {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.footer__first-column-links {
  display: block;
  color: #dedede;
  text-decoration: none;
}
.ask {
  font-size: 18px;
  margin-bottom: 24px;
}
.footer__column-title {
  font-size: 16px;
  text-transform: uppercase;
  color: white;
}
.footer__links-group {
  list-style-type: none;
  padding-left: 0;
  margin-top: 24px;
}
.footer__links-list-item {
  margin-bottom: 5px;
}
.footer__link {
  text-decoration: none;
  color: #dedede;
}
.footer__link:hover {
  color: white;
}
.footer__bottom {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 36px;
}
.footer__socials {
  display: flex;
  flex-direction: row;
  padding-left: 0;
  list-style-type: none;
}
.footer__social {
  margin-right: 12px;
}
.footer__social-icon {
  display: block;
}
.footer__social-icon-img {
  width: 28px;
  height: 28px;
}
.footer__bottom-container {
  display: flex;
  flex-direction: row;
}
.footer__bottom-text-wrapper {
  color: #d1d1d1;
  font-size: 14px;
}
.callfree {
  text-align: right;
  margin-right: 16px;
}
.mail {
  margin-left: 32px;
}
.footer__bottom-text {
}

.footer__phone {
  color: #f7f7f7;
  font-size: 30px;
  margin-right: 16px;
}
.footer__bottom-btn {
  outline: none;
  border: none;
  border-radius: 5px;
  background-color: #2c71c5;
  color: #ffffff;
  font-size: 16px;
  font-weight: bold;
  text-transform: uppercase;
  padding: 12px 24px;
  cursor: pointer;
}
.footer__lk-btn {
  border: 1px solid white;
  color: white;
  font-size: 16px;
  padding: 12px 24px;
  margin-bottom: 24px;
}
.footer__lk-btn:hover {
  background-color: rgba(0, 0, 0, 0.3);
}
</style>
