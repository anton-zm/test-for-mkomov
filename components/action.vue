<template>
  <section class="action">
    <content-wrapper class="action__wrapper">
      <div class="card">
        <div class="card__icon-round">
          <img src="mails.svg" alt="" class="card__icon" />
        </div>
        <h3 class="card__title">Информационная система</h3>
        <p class="card__subtitle">
          для улучшения коммуникации между жителями МКД и управляющей
          организацией
        </p>
      </div>
      <div class="card">
        <div class="card__icon-round">
          <img src="multiple-users.svg" alt="" class="card__icon" />
        </div>
        <h3 class="card__title">Обменивайтесь</h3>
        <p class="card__subtitle">
          с жителями МКД информацией и оперативно решайте вопросы управления МКД
        </p>
      </div>
      <div class="card">
        <div class="card__icon-round">
          <img src="conversation.svg" alt="" class="card__icon" />
        </div>
        <h3 class="card__title">Общайтесь</h3>
        <p class="card__subtitle">
          с управляющей организацией и ТСЖ, участвуйте в управлении своим домом
        </p>
      </div>
    </content-wrapper>
  </section>
</template>

<script>
import Content from '@/components/content'
export default {
  components: {
    'content-wrapper': Content,
  },
}
</script>

<style scoped>
.action {
  min-height: 512px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: radial-gradient(
    circle farthest-side at center bottom,
    #0091d7,
    #004094 100%
  );
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.5);
}
.action__wrapper {
  display: flex;
  flex-direction: row;
}
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: white;
}
.card__icon-round {
  background-color: white;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 92px;
  height: 92px;
}
.card__icon {
  width: 52px;
  height: 52px;
}
.card__title {
  text-align: center;
  font-size: 26px;
  font-weight: normal;
  margin-top: 24px;
}
.card__subtitle {
  text-align: center;
  margin-top: 10px;
  width: 75%;
}
</style>
