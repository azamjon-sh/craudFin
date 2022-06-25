<template>
  <button class="btn btn-blue" @click="loginShow">Войти</button>
  <LoginPage v-if="loginModal" @closeLogin="loginClose"/>

</template>

<script>
import LoginPage from "@/views/LoginPage";
export default {
  name: "HomePage",
  data(){
    return{
      loginModal:false,
    }
  },
  methods:{
    loginShow(){
      this.loginModal = true
    },
    loginClose(){
      this.loginModal = false
    }
  },
  components:{
    LoginPage
  }
}
</script>

<style scoped>

</style>