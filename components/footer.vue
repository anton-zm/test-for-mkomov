<template>
  <footer class="footer">
    <content-wrapper class="footer__content">
      <div class="footer__menu">
        <div class="footer__column">
          <Button class="footer__lk-btn" :btnText="'личный кабинет'" />
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
              v-for="(link, index) in column.group"
              :key="index"
              class="footer__link"
            >
              <nuxt-link :to="link.url">{{ link.text }}</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__bottom">
        <ul class="footer__socials">
          <li
            class="footer__social"
            v-for="(item, index) in socials"
            :key="index"
          >
            <a :href="item.url" :title="item.title" class="footer__social-icon"
              ><img :src="item.img" :alt="item.title"
            /></a>
          </li>
        </ul>
        <div class="footer__bottom-text-wrapper">
          <p class="footer__bottom-text">Наша почта:</p>
          <p class="footer__bottom-text footer__bottom-text_mail">
            mail@roskvartal.ru
          </p>
        </div>
        <div class="footer__bottom-text-wrapper">
          <p class="footer__bottom-text">Бесплатный звонок</p>
          <p class="footer__bottom-text footer__bottom-text_mail">
            по всей территории России
          </p>
        </div>
        <p class="footer__phone">8 800 500-65-61</p>
        <button class="footer__bottom-btn">заказать звонок</button>
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
          img: 'vk.png',
          title: 'Мы в Facebook',
        },
        {
          url: 'https://ok.ru/group/54946626666502',
          img: 'vk.png',
          title: 'Мы в Одноклассниках',
        },
        {
          url: 'https://www.youtube.com/channel/UC5t7A6P-Ewrug7zVyLOgUGg',
          img: 'vk.png',
          title: 'Мы на YouTube',
        },
        {
          url: 'https://twitter.com/roskvartal',
          img: 'vk.png',
          title: 'Мы в Twitter',
        },
        {
          url: 'https://live.viber.com/#/roskvartal',
          img: 'vk.png',
          title: 'Мы в Viber',
        },
        {
          url: 'https://t.me/roskvartal',
          img: 'vk.png',
          title: 'Мы в Telegram',
        },
      ],
    }
  },
}
</script>

<style scoped>
.footer {
}
.footer__content {
}
.footer__menu {
}
.footer__column {
}

.footer__first-column-links {
}
.ask {
}
.footer__column-title {
}
.footer__links-group {
}
.footer__link {
}
.footer__bottom {
}
.footer__socials {
}
.footer__social {
}
.footer__social-icon {
}
.footer__bottom-text-wrapper {
}
.footer__bottom-text {
}
.footer__bottom-text_mail {
}
.footer__phone {
}
.footer__bottom-btn {
}
.footer__lk-btn {
  border: 1px solid white;
  color: white;
}
.footer__lk-btn:hover {
  font-size: 18px;
  background-color: rgba(0, 0, 0, 0.3);
}
</style>
