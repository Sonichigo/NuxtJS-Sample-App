<template>
<div>
  <header>
    <div class="container">
      <nav
        class="navbar navbar-expand-lg navbar-light primary-menu"
        style="background-color: #fff">
        <Nuxt-link to="/login" />
        <a class="navbar-brand" href="#"><img class="navbar-logo" src="../assets/logo.jpg" /></a>
      <ul>
        <li style="float:right"><router-link to="/login">
          <button
            class="btn btn-lg btn-warning mt-3 cta"
            type="button"
            style="float:right"
          >Login
          </button></router-link>
          </li>
        <li style="float:right"><a href="#news">Contact Us</a></li>
        <li style="float:right"><a href="#contact">Resources</a></li>
        <li style="float:right"><a href="#news">Docs</a></li>
        <li style="float:right"><a href="#contact">Pricing</a></li>
        <li style="float:right"><a class="active" href="#home">Home</a></li>
        </ul>
      </nav>
    </div>
  </header>
  
  <main>
    <div class="heading">
      <h1>Product Headline</h1>
      <button class="btn btn-lg btn-warning mt-3 cta">
        <span>Call To Action</span>
      </button>
    </div>
    <div class="feature-cards row">
      <div class="col-xs-12 col-sm-6 col-md-4">
        <div class="card mb-4 mx-auto">
          <div class="card-body">
            <h4 class="card-title">Feature One</h4>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.<br/>
            <a href="#" class="btn1 btn-warning">Go somewhere</a>
            </p>
          </div>
        </div>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <div class="card mb-4 mx-auto">
          <div class="card-body">
            <h4 class="card-title">Feature Two</h4>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
              <br/>
            <a href="#" class="btn1 btn-warning">Go somewhere</a>
            </p>
          </div>
        </div>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <div class="card mb-4 mx-auto">
          <div class="card-body">
            <h4 class="card-title">Feature Three</h4>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.<br/>
            <a href="#" class="btn1 btn-warning">Go somewhere</a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </main>
  <Footer />
</div>
</template>

<script>
import Footer from "./Footer.vue";
export default {
  name: "LandingPage",
  components: {
    Footer,
  },
  methods: {
    home() {
      window.location.href = "/login";
    },
  },
};
</script>

<style>
.login {
  background-color: #ffa500;
  padding: 0.5rem;
}
.container {
  margin: 0;
  padding: 0;
  max-width: 100%;
  box-shadow: 0 8px 8px #888888;
}

body {
  background-image: url("../assets/bg.png");
  background-repeat: no-repeat;
  background-size: cover;
  overflow-x: hidden;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: white;
}

li a {
  display: block;
  color:#888888;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

.active {
  color: #1a1a1a;
}

.btn {
  background-color: #ffa500;
  border: none;
  color: black;
  padding: 13px 30px;
  text-align: center;
  display: inline-block;
  font-size: 16px;
  margin:1%;
  border-radius: 5px;
}

.btn1 {
  background-color: #ffa500;
  border: none;
  color: black;
  padding: 10px;
  text-align: center;
  display: inline-block;
  font-size: 16px;
  margin:1%;
  text-decoration: none;
  border-radius: 5px;
}

.nav {
  padding-left: 2% !important;
  padding-right: 2% !important;
}
.navbar-brand {
  width: 100px;
  height: 80px;
}

.navbar-logo {
  margin: 8px;
  height: 4em;
  width: 4em;
  float:left;
}

main {
  height: 500px;
}

.heading {
  margin-top: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.cta {
  transition: all 0.5s;
}

.cta span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.cta span:after {
  content: "\00bb";
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.cta:hover span {
  padding-right: 25px;
}

.cta:hover span:after {
  opacity: 1;
  right: 0;
}

.feature-cards {
  margin-top: 5rem;
  margin-bottom: 5rem;
  margin-left: 3rem;
  margin-right: 3rem;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
}

.nav-link:active{
color: #000000;
}

.card {
  margin-right: 3rem;
  background-color: #ffffff;
  width: 20em;
  height: 200px;
  font-family: "Open Sans", sans-serif;
}
.card-body{
  padding: 3% 3%;
  align-items: center;
}
</style>