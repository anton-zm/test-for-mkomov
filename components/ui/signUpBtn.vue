<template>
  <button @click="signup" class="signup-btn">{{ btnText }}</button>
</template>

<script>
export default {
  props: ['btnText'],
  methods: {
    signup() {
      this.$router.push('/signup')
    },
  },
}
</script>

<style scoped>
.signup-btn {
  padding: 16px 20px;
  background-color: #e12351;
  color: #ffffff;
  font-size: 13px;
  font-weight: bold;
  text-transform: uppercase;
  line-height: 16px;
  border-radius: 5px;
  border: none;
  outline: none;
  cursor: pointer;
  transition: transform 0.1s ease-in-out;
}
.signup-btn:hover {
  transform: translateY(-5px);
}
</style>
