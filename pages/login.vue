<template>
  <section>
    <div class="login-container">
    <h1 class="title">{{ currentTitle }}</h1>
    <div class="loggedin" v-if="isLoggedIn">Hello User</div>
    <div class="formContainer" id="sawo-container" v-if="!isLoggedIn">
      <!-- The div in which sawo form is displayed -->
    </div>
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
.container img {
  flex: 0.6;
  object-fit: contain;
}

#sawo-container {
  height: 400px;
  width: 300px;
}
.login-container {
  flex: 0.4;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  max-width: 400px;
  min-height: 400px;
  padding: 20px;
  margin-left:30%;
  border-radius: 10px;
  border: 1px solid grey;
  background-color: #fff;
  height : 80%;
  color: #000;
}

.login-container h1 {
  font-weight: 500;
  font-size: 40px;
  line-height: 48px;
  color: #1f1e1e;
}

.login-container p {
  padding: 0 10px 0 10px;
  text-align: center;
}


@media (max-width: 400px) {
  .container img {
    display: none;
  }

  .login-container {
    border: none;
    flex: 1;
  }

  #sawo-container {
    /* height: 500px; */
    background-color: #bcedef;
    width: 100%;
  }
}
</style>