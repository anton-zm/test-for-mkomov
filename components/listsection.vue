<template>
  <section class="list">
    <content-wrapper class="list__wrapper">
      <img
        src="img_mnogokvartir.svg"
        alt="Жители многоквартирных домов"
        class="list__img mkd"
      />
      <div class="list__center-cont">
        <List
          :array="mkd"
          :title="'Жители многоквартирных домов'"
          :btnText="'зарегистрировать личный кабинет'"
        />
      </div>
    </content-wrapper>
    <content-wrapper class="list__wrapper">
      <div class="list__center-cont">
        <List
          :array="uk"
          :title="'Управляющие организации и ТСЖ'"
          :btnText="'зарегистрироваться'"
        />
      </div>
      <img
        src="img_upr_company.svg"
        alt="Управляющие организации и ТСЖ"
        class="list__img uk"
      />
    </content-wrapper>
  </section>
</template>

<script>
import Content from '@/components/content'
import SignUpBtn from '@/components/ui/signUpBtn'
import List from '@/components/textList'
export default {
  components: {
    'content-wrapper': Content,
    List,
  },
  data() {
    return {
      uk: [
        'Быстрое и надёжное информирование жителей МКД',
        'Работа с обращениями',
        'Возможность прикрепления фото- и видеоматериалов',
        'Получение заявок на выполнение работ',
        'Обратная связь от жителей МКД',
        'Контроль потребления коммуналных ресурсов',
        'Предложение дополнительных платных услуг УО',
        'Размещение новостей и отчётов',
        'Автоматическая синхронизация вашего сайта с ГИС ЖКХ',
        'Приём платежей за ЖКУ',
      ],
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
  padding: 48px 0;
}
.list__center-cont {
  display: flex;
  align-items: center;
}
.list__wrapper {
  display: flex;
  flex-direction: row;
  margin-top: 30px;
}

.list__img {
  margin: 0 44px;
}
.uk {
  height: 546px;
}
.mkd {
  height: 676px;
}
</style>
