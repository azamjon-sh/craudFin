<template>
  <header class="header">
    <div class="row">
      <div class="header__inner">
        <div class="header__left">
          <div class="header__logo">
            <a href="#" @click.prevent>КраудФин</a>
          </div>
          <div class="header__menu">
            <div class="header__item">
              <span>Собрать средства</span>
              <img src="@/assets/img/global/arrow-down.svg" alt="">
            </div>
            <div class="header__item">
              <span>Инвестировать</span>
              <img src="@/assets/img/global/arrow-down.svg" alt="">
            </div>
            <div class="header__item header__phone">
              <img src="@/assets/img/global/phone.svg" alt="">
              <span>8 800 700 80 80</span>
            </div>
          </div>
        </div>
        <div class="header__right">
          <button class="btn btn-blue header__btn" @click="$emit('loginShow')">Войти</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent"
}
</script>

<style scoped>

</style>