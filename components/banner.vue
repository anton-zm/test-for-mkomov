<template>
  <section class="banner">
    <content-wrapper>
      <div class="banner__wrapper">
        <h1 class="banner__title">
          Приложение для решения текущих вопросов по дому онлайн
        </h1>
        <p class="banner__subtitle">
          Поможет решить проблемы жителей дома в режиме реального времени, без
          дополнительных визитов и звонков в управляющую организацию
        </p>
        <SignUpBtn class="banner__signup" :btnText="'попробовать бесплатно'" />
        <div class="banner__share">
          <ShareBtn
            :img="'apple.png'"
            :source="'app store'"
            :link="'https://apps.apple.com/ru/app/%D0%BC%D0%BE%D1%8F-%D0%BA%D0%B2%D0%B0%D1%80%D1%82%D0%B8%D1%80%D0%B0/id1489456308'"
          />
          <ShareBtn
            :img="'googleplay.png'"
            :source="'google play'"
            :link="'https://play.google.com/store/apps/details?id=ru.roskvartal.myApartment.android&hl=ru'"
          />
        </div>
      </div>
    </content-wrapper>
  </section>
</template>

<script>
import Content from '@/components/content'
import SignUpBtn from '@/components/ui/signUpBtn'
import ShareBtn from '@/components/ui/shareBtn'
export default {
  components: {
    'content-wrapper': Content,
    SignUpBtn,
    ShareBtn,
  },
  methods: {},
}
</script>

<style scoped>
.banner {
  background-image: url('../static/main.png');
  background-position-x: 50%;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 54px 0;
}
.banner__wrapper {
  width: 50%;
  margin-left: 40px;
}
.banner__title {
  font-size: 34px;
  line-height: 44px;
}
.banner__subtitle {
  margin-top: 17px;
  font-size: 22px;
  line-height: 26px;
}
.banner__share {
  display: flex;
  flex-direction: row;
  margin-top: 18px;
}
.banner__signup {
  margin-top: 44px;
}
</style>
