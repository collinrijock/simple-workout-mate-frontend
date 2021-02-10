<template>
  <div id="login-handler-container">
    <input class="form-field" type="text" v-model="username" placeholder="Username">
    <input class="form-field" type="text" v-model="password" placeholder="Password">
    <button id="submit" @click="submitLogin">Log in</button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import axios from 'axios';

@Component
export default class LoginHandler extends Vue {
  username: String = ""
  password: String = ""
  apiUrl: String = "http://127.0.0.1:8000/"
  async submitLogin () {
    let response = await axios.get(this.apiUrl + 'login', {
      headers: {
        'Access-Control-Allow-Origin' : '*'
      },
      data: {
        username: this.username,
        password: this.password
      }
    })
  }
}
</script>

<style scoped lang="scss">
#login-handler-container {
  height: 20vh;
  width: 20vw;
  display: flex;
  flex-flow: column nowrap;
}
</style>
