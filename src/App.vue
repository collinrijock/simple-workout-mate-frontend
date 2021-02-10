<template>
  <div id="app">
    <LoginHandler></LoginHandler>
    <SignupHandler></SignupHandler>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import LoginHandler from '@/components/LoginHandler.vue'; // @ is an alias to /src
import SignupHandler from '@/components/SignupHandler.vue'; // @ is an alias to /src


@Component({
  components: {
    LoginHandler,
    SignupHandler
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  width: 100vw;
}

</style>
