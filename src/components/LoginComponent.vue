<template>
  <div class="login__wrapper">
    <div class="login__block">
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
      <div class="login__field">
        <label class="login__label" for="email">Email</label>
        <input type="email" class="login__input" id="email" placeholder="Введите email">
      </div>
      <div class="login__field">
        <label class="login__label" for="password">Пароль</label>
        <input type="password" class="login__input" id="password" placeholder="Введите пароль">
      </div>
      <a href="#" @click.prevent class="link login__link">Забыли пароль?</a>
      <button class="btn btn-blue login__submit"><span>Войти</span></button>
      <div class="login__line"><span>Или</span></div>
      <button class="btn btn-light-blue login__methods">
        <span>Войти через VK</span>
      </button>
      <button class="btn btn-light-blue login__methods">
        <span>Войти с помощью УКЭП</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginComponent",
  data() {
    return {
      forms: {
        loginForm: true,
        authForm: false,
      }
    }
  },
  methods: {
    changeForm(target) {
      if (target == 'login') {
        this.forms.loginForm = true
        this.forms.authForm = false
      } else if (target == 'auth') {
        this.forms.loginForm = false
        this.forms.authForm = true
      }
    }
  }
}
</script>

<style scoped>

</style>