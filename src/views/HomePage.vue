<template>
  <HeaderComponent @loginShow="loginShow"/>
  <main class="main">
    <IntroComponent/>
    <ProjectsComponent/>
    <QuestionsComponent/>
    <InvestmentComponent/>
    <QuestionsComponent/>
  </main>
  <FooterComponent />
  <LoginPage v-if="loginModal" @closeLogin="loginClose"/>
</template>

<script>
import HeaderComponent from "@/components/HeaderComponent";
import LoginPage from "@/views/LoginPage";
import IntroComponent from "@/components/IntroComponent";
import ProjectsComponent from "@/components/ProjectsComponent";
import QuestionsComponent from "@/components/QuestionsComponent";
import InvestmentComponent from "@/components/InvestmentComponent";
import FooterComponent from "@/components/FooterComponent";
export default {
  name: "HomePage",
  data() {
    return {
      loginModal: false,
    }
  },
  methods: {
    loginShow() {
      this.loginModal = true
    },
    loginClose() {
      this.loginModal = false
    }
  },
  components: {
    LoginPage,
    HeaderComponent,
    IntroComponent,
    ProjectsComponent,
    QuestionsComponent,
    InvestmentComponent,
    FooterComponent
  }
}
</script>

<style scoped>

</style>