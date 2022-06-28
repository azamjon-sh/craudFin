<template>
  <div class="projects__item">
    <div class="projects__img" :style="`background-image: url(${item.img})`">
      <div class="btn btn-light-blue projects__looking" :class="active?'active':''"
           @click="active = !active">
        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" clip-rule="evenodd"
                d="M5.83337 3.33317C5.61236 3.33317 5.4004 3.42097 5.24412 3.57725C5.08784 3.73353 5.00004 3.94549 5.00004 4.1665V15.8805L9.51568 12.6551C9.80542 12.4481 10.1947 12.4481 10.4844 12.6551L15 15.8805V4.1665C15 3.94549 14.9122 3.73353 14.756 3.57725C14.5997 3.42097 14.3877 3.33317 14.1667 3.33317H5.83337ZM4.06561 2.39874C4.53445 1.9299 5.17033 1.6665 5.83337 1.6665H14.1667C14.8297 1.6665 15.4656 1.9299 15.9345 2.39874C16.4033 2.86758 16.6667 3.50346 16.6667 4.1665V17.4998C16.6667 17.812 16.4923 18.098 16.2147 18.2408C15.9371 18.3836 15.603 18.3594 15.349 18.1779L10 14.3573L4.65107 18.1779C4.39706 18.3594 4.06295 18.3836 3.78539 18.2408C3.50783 18.098 3.33337 17.812 3.33337 17.4998V4.1665C3.33337 3.50346 3.59677 2.86758 4.06561 2.39874Z"
                fill="#3589CF"/>
        </svg>
        <span>Отслеживать</span>
      </div>
    </div>
    <div class="project__body">

      <h4 class="h4 project__name">
        {{ item.name }}
      </h4>

      <div class="project__text">
        {{ item.text }}
      </div>
      <div class="project__top">
        <span class="project__type">
          {{ item.type }}
        </span>
      </div>
      <div class="project__parameters">
        <div class="project__target">
          Цель<span>{{ item.target }} ₽</span>
        </div>
        <div class="project__target">
          Собрано<span>{{ item.current }} ₽</span>
        </div>
        <div class="project__target">
          Доля<span>{{ item.share }} %</span>
        </div>
      </div>
      <div class="project__progress">
        <div :style="'width:' + (item.current * 100 / item.target) + '%'"></div>
      </div>
      <div class="project__date">
        Осталось 5 дней
      </div>
      <button class="btn btn-light-blue btn-icon project__btn">
        <span>Подробнее</span>
        <img src="@/assets/img/project/arrow-next.svg" :alt="item.name">
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: ['item'],
  name: "InvestItem",
  data() {
    return {
      active: false,
    }
  }
}
</script>

<style scoped>

</style>