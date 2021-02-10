<template>
  <div id="signup-handler-container">
    <input class="form-field" type="text" v-model="username" placeholder="Username">
    <input class="form-field" type="text" v-model="password" placeholder="Password">
    <input class="form-field" type="text" v-model="password" placeholder="Retype Password">
    <button id="submit" @click="submitLogin">Log in</button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import axios from 'axios';

@Component
export default class SignupHandler extends Vue {
  username: String = ""
  passworda: String = ""
  passwordb: String = ""
  apiUrl: String = "http://127.0.0.1:8000/"
}
</script>

<style scoped lang="scss">
#signup-handler-container {
  height: 20vh;
  width: 20vw;
  display: flex;
  flex-flow: column nowrap;
}
</style>
