<template>
  <main class="success">
    <div class="success__container">
      <h1 class="success__title">Поздравляем!</h1>
      <p class="success___subtitle">
        Вы успешно зарегистрировались на нашем портале!
      </p>
      <nuxt-link class="success__button" to="/">На главную</nuxt-link>
    </div>
  </main>
</template>

<script>
export default {}
</script>

<style scoped>
.success {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #aa9f9f;
  min-height: 80vh;
}
.success__container {
  width: 300px;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white;
  text-align: center;
  padding: 30px;
  box-shadow: black 2px 2px 10px;
}
.success__title {
  color: #9c9595;
}
.success___subtitle {
  margin-top: 24px;
  color: #9c9595;
}
.success__button {
  margin-top: 24px;
  display: block;
  background-color: orange;
  border-radius: 5px;
  color: white;
  padding: 12px;
  text-decoration: none;
}
</style>
