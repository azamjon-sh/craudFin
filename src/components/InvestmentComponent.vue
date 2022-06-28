<template>
  <section class="projects invest">
    <div class="row">
      <div class="projects__inner">
        <h2 class="h2 projects__title">
          Инвестиционные предложения
        </h2>
        <div class="projects__subtitle">
          Предварительные проекты - это проекты, по которым изучается подтенциальный спрос инвесторов.<br>
          Оцените проект и проявите заинтересованность, нажав на кнопку “Интересно!”.
        </div>
        <div class="projects__list">
          <InvestItem v-for="item in investList" :item="item" :key="item.id"/>
        </div>
        <button class="btn btn-blue btn-icon projects__all"><span>Смотреть все проекты</span>
          <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd"
                  d="M16.6668 10.0002C16.6668 10.4604 16.2937 10.8335 15.8335 10.8335L4.16683 10.8335C3.70659 10.8335 3.3335 10.4604 3.3335 10.0002C3.3335 9.53993 3.70659 9.16683 4.16683 9.16683L15.8335 9.16683C16.2937 9.16683 16.6668 9.53992 16.6668 10.0002Z"
                  fill="#fff"/>
            <path fill-rule="evenodd" clip-rule="evenodd"
                  d="M16.4228 9.41091C16.7482 9.73634 16.7482 10.264 16.4228 10.5894L10.5894 16.4228C10.264 16.7482 9.73635 16.7482 9.41091 16.4228C9.08547 16.0973 9.08547 15.5697 9.41091 15.2442L14.655 10.0002L9.41091 4.75609C9.08547 4.43065 9.08547 3.90301 9.41091 3.57757C9.73634 3.25214 10.264 3.25214 10.5894 3.57757L16.4228 9.41091Z"
                  fill="#fff"/>
          </svg>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
import InvestItem from "@/components/Invest/InvestItem";

export default {
  name: "InvestmentComponent",
  components: {InvestItem},
  data() {
    return {
      investList: [
        {
          id: 1,
          img: require('@/assets/img/project/1.png'),
          name: 'Название проекта',
          text: 'Этот проект - отличная бизнес идея и&nbsp;уникальная команда. Отличное вложение важих средств! ',
          type: 'Выпуск УЦП',
          target: 1000000,
          current: 500000,
          share: 5.65,
        },
        {
          id: 2,
          img: require('@/assets/img/project/2.png'),
          name: 'Название проекта',
          text: 'Этот проект - отличная бизнес идея и&nbsp;уникальная команда. Отличное вложение важих средств! ',
          type: 'Конвертируемый займ',
          target: 1000000,
          current: 500000,
          share: 5.65,
        },
        {
          id: 3,
          img: require('@/assets/img/project/3.png'),
          name: 'Название проекта',
          text: 'Этот проект - отличная бизнес идея и&nbsp;уникальная команда. Отличное вложение важих средств! ',
          type: 'Выпуск акций',
          target: 1000000,
          current: 500000,
          share: 5.65,
        },
        {
          id: 4,
          img: require('@/assets/img/project/4.png'),
          name: 'Название проекта',
          text: 'Этот проект - отличная бизнес идея и&nbsp;уникальная команда. Отличное вложение важих средств! ',
          type: 'Займ',
          target: 1000000,
          current: 500000,
          share: 5.65,
        },
      ]
    }
  },
}
</script>

<style scoped>

</style>