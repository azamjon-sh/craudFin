<template>
  <section class="question">
    <div class="row">
      <div class="question__inner">
        <h2 class="h2 question__title">Вопросы по предварительным проектам</h2>
        <div class="question__subtitle">
          Предварительные проекты - это проекты, по которым изучается подтенциальный спрос инвесторов.<br>
          Оцените проект и проявите заинтересованность, нажав на кнопку “Интересно!”.
        </div>
        <div class="question__list">
          <QuestionItem v-for="question in questionList"
                        :question="question"
                        :key="question.id"
                        @activeQuestion="activeQuestion"/>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import QuestionItem from "@/components/question/QuestionItem";

export default {
  name: "questionsComponent",
  data() {
    return {
      questionList: [
        {
          id: 1,
          name: 'What do you call a dog that tells time?',
          text: 'Sushi!! Most Westerners immediately hear that word and think of raw fish (what you are really talking about is sashimi), but actually the term sushi just refers to the type of vinegar rice used in the traditional Japanese cuisine. The great thing about sushi is that I can easily fill up and satiate my hunger, but I never feel overstuffed.',
          active: false,
        },
        {
          id: 2,
          name: 'What was improved since the last review?',
          text: 'Sushi!! Most Westerners immediately hear that word and think of raw fish (what you are really talking about is sashimi), but actually the term sushi just refers to the type of vinegar rice used in the traditional Japanese cuisine. The great thing about sushi is that I can easily fill up and satiate my hunger, but I never feel overstuffed.',
          active: false,
        },
        {
          id: 3,
          name: 'Who is the target audience?',
          text: 'Sushi!! Most Westerners immediately hear that word and think of raw fish (what you are really talking about is sashimi), but actually the term sushi just refers to the type of vinegar rice used in the traditional Japanese cuisine. The great thing about sushi is that I can easily fill up and satiate my hunger, but I never feel overstuffed.',
          active: false,
        },
        {
          id: 4,
          name: 'Can we make icons more obvious?',
          text: 'Sushi!! Most Westerners immediately hear that word and think of raw fish (what you are really talking about is sashimi), but actually the term sushi just refers to the type of vinegar rice used in the traditional Japanese cuisine. The great thing about sushi is that I can easily fill up and satiate my hunger, but I never feel overstuffed.',
          active: false,
        },
        {
          id: 5,
          name: 'What is the problem that you tried to solve?',
          text: 'Sushi!! Most Westerners immediately hear that word and think of raw fish (what you are really talking about is sashimi), but actually the term sushi just refers to the type of vinegar rice used in the traditional Japanese cuisine. The great thing about sushi is that I can easily fill up and satiate my hunger, but I never feel overstuffed.',
          active: false,
        },
        {
          id: 6,
          name: 'Do you think anybody is going to click that?',
          text: 'Sushi!! Most Westerners immediately hear that word and think of raw fish (what you are really talking about is sashimi), but actually the term sushi just refers to the type of vinegar rice used in the traditional Japanese cuisine. The great thing about sushi is that I can easily fill up and satiate my hunger, but I never feel overstuffed.',
          active: false,
        },
      ],
    }
  },
  methods: {
    activeQuestion(id) {

      this.questionList.forEach((item) => {
        if (item.id != id) {

          item.active = false
        }
      });
      let target = this.questionList.find(item => item.id == id).active
      this.questionList.find(item => item.id == id).active = !target;
    },
  },
  components: {
    QuestionItem,
  }
}
</script>

<style scoped>

</style>