<script>
import Board from './components/board.vue'
import Login from './components/login.vue'

export default {
    name: "App",
    data() {
      return {
        isAuth: false,
        users: [
          {
            login: 'admin',
            password: 'admin',
            avatar: 'https://cdn-icons-png.flaticon.com/512/5556/5556468.png'
          }
        ]
      }
    },
    methods: {
      login(){
        console.log('Авторизация');
      }
    },
    components:{
      Board,
      Login
    }
}
</script>

<template>
  <Board test='Тестовый входящий параметр' v-if="isAuth"/>
  <Login :handlerLogin='login' v-else/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>