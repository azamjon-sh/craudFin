<template>
  <div class="login__wrapper">
    <div class="login__block">
      <div class="login__head" v-if="forms.head">
        <h3 class="login__title">Вход в систему</h3>
        <div class="login__top">
          <button class="login__button" :class="forms.loginForm?'active':''"
                  @click="changeForm('login')">
            Вход
          </button>
          <button class="login__button" :class="forms.authForm?'active':''"
                  @click="changeForm('auth')">
            Регистрация
          </button>
        </div>
      </div>
      <LoginComponent v-if="forms.loginForm"/>
      <RegistComponent v-if="forms.authForm" @openStep2="openStep2" @closeStep2="closeStep2"/>
      <div class="login__close" @click="$emit('closeLogin')">
        <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M22.6592 11.2305C23.181 10.7088 23.181 9.86287 22.6592 9.34113C22.1375 8.81939 21.2916 8.81939 20.7698 9.34113L16.0002 14.1107L11.2306 9.34113C10.7089 8.81939 9.863 8.81939 9.34126 9.34113C8.81952 9.86287 8.81952 10.7088 9.34126 11.2305L14.1108 16.0001L9.34126 20.7697C8.81952 21.2914 8.81952 22.1374 9.34126 22.6591C9.863 23.1808 10.7089 23.1808 11.2306 22.6591L16.0002 17.8895L20.7698 22.6591C21.2916 23.1808 22.1375 23.1808 22.6592 22.6591C23.181 22.1374 23.181 21.2914 22.6592 20.7697L17.8896 16.0001L22.6592 11.2305Z"
              fill="#7D7D7D"/>
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
import LoginComponent from "@/components/login/LoginComponent";
import RegistComponent from "@/components/login/RegistComponent";

export default {
  name: "LoginPage",
  data() {
    return {
      forms: {
        loginForm: true,
        authForm: false,
        head: true,
      }
    }
  },
  methods: {
    changeForm(target) {
      if (target === 'login') {
        this.forms.loginForm = true
        this.forms.authForm = false
      } else if (target === 'auth') {
        this.forms.loginForm = false
        this.forms.authForm = true
      }
    },
    openStep2() {
      this.forms.head = false
    },
    closeStep2() {
      this.forms.head = true
    }
  },
  components: {
    LoginComponent, RegistComponent
  }
}
</script>

<style scoped>

</style>