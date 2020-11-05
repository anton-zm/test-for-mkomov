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
  data() {
    return {
      mkd: [
        'Получение сведений о квартире, доме, лицевом счёте и управляющей организации',
        'Отправка обращений или вопроса в управляющую организацию, ТСЖ или ЖСК',
        'Передача показаний счётчиков',
        'Вызов аварийной службы',
        'Запись на приём к руководителю управляющей организации',
        'Новости дома и района',
        'Публикация объявлений для жителей вашего дома',
        'Отправка заявок на устранение проблемы и оценка качества её выполнения',
        'Организация совместных мероприятий с управляющей организацией',
      ],
    }
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
