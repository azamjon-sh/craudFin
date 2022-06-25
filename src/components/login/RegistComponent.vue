<template>
  <div v-if="regist.firstStep">
    <div class="login__field">
      <label class="login__label" for="email">Email</label>
      <input type="email" class="login__input" id="email" placeholder="Введите email">
    </div>

    <div class="login__field">
      <label class="login__label" for="password">Пароль</label>
      <input type="password" class="login__input" id="password" placeholder="Введите пароль">
    </div>

    <div class="login__field">
      <label class="login__label" for="confirm-pass">Подвердите пароль</label>
      <input type="password" class="login__input" id="confirm-pass" placeholder="Введите пароль ещё раз">
    </div>

    <div class="login__captcha">
      <div class="login__captcha-img">
        Капча
      </div>
      <div class="login__field">
        <label class="login__label" for="captcha-val">Проверочный код (слева)</label>
        <input type="password" class="login__input" id="captcha-val" placeholder="Введите код с картинки слева">
      </div>
    </div>

    <button class="btn btn-blue btn-icon login__submit" @click="continueRegist">
      <span>Зарегистрироваться</span>
      <img src="@/assets/img/arrow.svg" alt="">
    </button>

    <div class="login__line"><span>Или</span></div>

    <button class="btn btn-light-blue login__methods">
      <span>Зарегистрироваться через VK</span>
    </button>

    <button class="btn btn-light-blue login__methods">
      <span>Зарегистрироваться с помощью УКЭП</span>
    </button>
  </div>
  <div v-if="regist.secondStep" class="login__step2">
    <h3 class="login__title">Регистрация</h3>
    <div class="login__field">
      <label class="login__label" for="secondName">Фамилия</label>
      <input type="text" class="login__input" id="secondName" placeholder="Введите фамилию">
    </div>
    <div class="login__field">
      <label class="login__label" for="firstName">Имя</label>
      <input type="text" class="login__input" id="firstName" placeholder="Введите имя">
    </div>
    <div class="login__field">
      <label class="login__label" for="fatherName">Отчество (не обязательно)</label>
      <input type="text" class="login__input" id="fatherName" placeholder="Введите отчество">
    </div>
    <div class="login__field">
      <label class="login__label" for="birthday">Дата рождения</label>
      <input type="text" class="login__input" id="birthday" placeholder="Введите дату рождения">
    </div>
    <div class="login__field">
      <input type="checkbox" class="login__checkbox" id="rules">
      <label class="login__label" for="rules"><span>Я согласен с
        <span class="link">Правилами Платформы</span></span></label>
    </div>
    <div class="login__field">
      <input type="checkbox" class="login__checkbox" id="processing">
      <label class="login__label" for="processing">
        <span>Я даю <span class="link">Согласие на обработку персональных данных</span></span>
      </label>
    </div>
    <button class="btn btn-blue btn-icon login__submit">
      <span>Зарегистрироваться</span>
    </button>
    <button class="btn btn-light-blue login__methods" @click="backRegist">
      <span>Назад</span>
    </button>
  </div>
</template>

<script>
export default {
  name: "LoginComponent",
  data() {
    return {
      regist: {
        firstStep: true,
        secondStep: false,
      }
    }
  },
  methods: {
    continueRegist() {
      this.regist.firstStep = false
      this.regist.secondStep = true
      this.$emit('openStep2')
    },
    backRegist(){
      this.regist.firstStep = true
      this.regist.secondStep = false
      this.$emit('closeStep2')
    }
  }
}
</script>

<style scoped>

</style>