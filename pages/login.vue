<template>
  <section>
    <h2 class="title">{{ currentTitle }}</h2>
    <div class="loggedin" v-if="isLoggedIn">Hello User</div>
    <div class="formContainer" id="sawo-container" v-if="!isLoggedIn">
      <!-- The div in which sawo form is displayed -->
    </div>
  </section>
</template>

<script>
import Sawo from 'sawo'
export default {
  name: 'Sawo',
  data: () => ({
    isLoggedIn: false,
    currentTitle: 'Login Page',
    userPayload: {},
    Sawo: null,
  }),
  mounted() {
    const config = {
      // should be same as the id of the container
      containerID: 'sawo-container',
      // can be one of 'email' or 'phone_number_sms'
      identifierType: 'email',
      // Add the API key
      apiKey: '73779307-b876-4454-b7a2-d7863a603e17',
      // Add a callback here to handle the payload sent by sdk
      onSuccess: (payload) => {
        this.userPayload = payload
        this.isLoggedIn = true
        this.currentTitle = 'Dashboard'
      },
    }
    this.Sawo = new Sawo(config)
    this.Sawo.showForm()
  },
}
</script>

<style>
#sawo-container {
  width: 400px;
  height: 400px;
}
</style>