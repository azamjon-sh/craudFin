<template>
  <HeaderComponent @loginShow="loginShow"/>
  <main class="main">
    <IntroComponent/>
    <ProjectsComponent/>
  </main>
  <LoginPage v-if="loginModal" @closeLogin="loginClose"/>
</template>

<script>
import HeaderComponent from "@/components/HeaderComponent";
import LoginPage from "@/views/LoginPage";
import IntroComponent from "@/components/IntroComponent";
import ProjectsComponent from "@/components/ProjectsComponent";

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
    LoginPage, HeaderComponent, IntroComponent, ProjectsComponent
  }
}
</script>

<style scoped>

</style>