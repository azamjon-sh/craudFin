<template>
  <div>
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
</template>

<script>
export default {
  name: "LoginComponent"
}
</script>

<style scoped>

</style>