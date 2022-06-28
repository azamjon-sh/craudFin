<template>
  <footer class="footer">
    <div class="row">
      <div class="footer__inner">
        <div class="footer__left">
          <div class="footer__logo">
            <a href="#" @click.prevent>КраудФин</a>
          </div>
          <div class="footer__info">Инвестиционная платформа Московского региона</div>
          <div class="footer__info">Оператор – ООО «Краудфандинговые технологии»</div>
          <div class="footer__info">8 800 700 80 80</div>
          <div class="footer__info">kraudfin@info.ru</div>
          <div class="footer__info">№ _________ в реестре операторов инвестиционных платформ ЦБ РФ</div>

        </div>
        <div class="footer__menu">
          <div class="footer__item" v-for="item in footerList">
            <div class="footer__title">{{item.title}}</div>
            <a class="footer__points" :href="elem.url" v-for="elem in item.points">{{elem.name}}</a>
          </div>
        </div>
      </div>
      <div class="footer__copyright">
        © 2022 КраудФин. Все права зарезервированы.
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data() {
    return {
      footerList: [
        {
          title: 'О платформе',
          points: [
            {
              url: '#',
              name: 'О нас'
            },
            {
              url: '#',
              name: 'Контакты'
            },
            {
              url: '#',
              name: 'Новости'
            },
            {
              url: '#',
              name: 'Тарифы'
            },
            {
              url: '#',
              name: 'Акции'
            },
          ]
        },
        {
          title: 'Инвесторам',
          points: [
            {
              url: '#',
              name: 'Инвестировать'
            },
            {
              url: '#',
              name: 'Как это работает'
            },
            {
              url: '#',
              name: 'ЧАВО'
            },
            {
              url: '#',
              name: 'Декларация о рисках'
            },
            {
              url: '#',
              name: 'Энциклопедия инвестора'
            },
          ]
        },
        {
          title: 'Предпринимателям',
          points: [
            {
              url: '#',
              name: 'Собрать деньги'
            },
            {
              url: '#',
              name: 'Как это работает'
            },
            {
              url: '#',
              name: 'ЧАВО'
            },
            {
              url: '#',
              name: 'Энциклопедия предпринимателя'
            },
            {
              url: '#',
              name: 'Услуги партнеров'
            },
          ]
        },
        {
          title: 'Правовая часть',
          points: [
            {
              url: '#',
              name: 'Раскрытие информации'
            },
            {
              url: '#',
              name: 'Политика обработки ПД'
            },
            {
              url: '#',
              name: 'Безопасность'
            },
            {
              url: '#',
              name: 'Типовые документы инвестору'
            },
            {
              url: '#',
              name: 'Типовые документы предпринимателю'
            },
          ]
        },
      ]
    }
  }
}
</script>

<style scoped>

</style>