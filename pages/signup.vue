<template>
  <main>
    <content-wrapper>
      <form @submit.prevent="submit" class="form">
        <label for="email" class="form__label">Адрес эл. почты</label>
        <input
          type="text"
          class="form__input"
          id="email"
          v-model="email"
          required
        />
        <label for="password" class="form__label">Пароль</label>
        <input
          type="text"
          class="form__input"
          id="password"
          v-model="password"
          required
        />
        <label for="city" class="form__label">Город</label>
        <select class="form__input" name="" id="city" v-model="city">
          <option value="0">Выберите из списка</option>
          <option v-for="item in cities" :key="item.id" :value="item.id">
            {{ item.city }}
          </option>
        </select>
        <div class="form__checkbox">
          <input type="checkbox" v-model="personal" id="personal" />
          <label class="form__chackbox-label" for="personal"
            >Согласен с условиями обработки перс. данных</label
          >
        </div>

        <button class="form__button" type="submit">Отправить</button>
      </form>
    </content-wrapper>
  </main>
</template>

<script>
import Content from '@/components/content'
import axios from 'axios'
export default {
  components: {
    'content-wrapper': Content,
  },

  beforeMount() {
    axios
      .get('https://5f3a6e3b2300b100169a8b93.mockapi.io/api/v1/cities')
      .then((res) => {
        this.cities = res.data
      })
      .catch((err) => {
        console.log(err)
        alert('Что-то пошло не так')
      })
  },

  methods: {
    submit() {
      if (!this.city) {
        alert('Нужно выбрать город')
        return
      }
      if (this.personal) {
        return axios
          .post('https://5f3a6e3b2300b100169a8b93.mockapi.io/api/v1/users', {
            email: this.email,
            password: this.password,
            cityId: this.city,
          })
          .then(this.$router.push('/success'))
      } else {
        alert(
          'Без согласия на обработку перс. данных зарегистрироваться, к сожалению, не получится'
        )
      }
    },
  },
  data() {
    return {
      email: '',
      password: '',
      city: '',
      personal: false,
      cities: [],
    }
  },
}
</script>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
  padding: 60px 0;
}
.form__label {
  margin-top: 20px;
}
.form__checkbox {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 20px;
}
.form__chackbox-label {
  margin-left: 10px;
}
.form__input {
  outline: none;
  border: solid 1px #cec5c5;
  border-radius: 5px;
  padding: 15px 10px;
  margin-top: 10px;
  font-size: 18px;
}
.form__button {
  outline: none;
  border: none;
  color: white;
  font-size: 16px;
  font-weight: bold;
  background-color: blue;
  border-radius: 5px;
  padding: 12px 20px;
  width: 120px;
  margin-top: 20px;
  cursor: pointer;
}
</style>
