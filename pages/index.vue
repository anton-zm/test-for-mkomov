<template>
  <main class="main">
    <Banner />
    <Action />
    <Title class="section-title" :title="'кто может пользоваться'" />
    <ListSection
      :array="mkd"
      :title="'Жители многоквартирных домов'"
      :btnText="'зарегистрировать личный кабинет'"
      :imgSrc="'img_mnogokvartir.svg'"
    />
  </main>
</template>

<script>
import Banner from '@/components/banner'
import Action from '@/components/action'
import Title from '@/components/sectionTitle'
import ListSection from '@/components/listsection'
export default {
  components: {
    Banner,
    Action,
    Title,
    ListSection,
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
.section-title {
  margin: 48px auto;
}
</style>
