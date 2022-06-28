<template>
  <div class="question__item" :class="question.active? 'active' : ''">
    <div class="question__top" @click="$emit('activeQuestion',question.id)">
      <svg class="question__icon" width="24" height="25" viewBox="0 0 24 25" fill="none"
           xmlns="http://www.w3.org/2000/svg">
        <g opacity="0.54">
          <path d="M6 9.93457L12 15.9346L18 9.93457" stroke="#3589CF" stroke-width="2" stroke-linecap="round"
                stroke-linejoin="round"/>
        </g>
      </svg>
      <div class="question__name">{{ question.name }}</div>
    </div>
    <div class="question__text">
      {{ question.text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "QuestionItem",
  props: ['question'],
}
</script>

<style scoped>

</style>