<template>
<div>
  <header>
    <div class="container">
      <nav
        class="navbar navbar-expand-lg navbar-light primary-menu"
        style="background-color: #fff">
        <a class="navbar-brand" href="#">
          <img class="navbar-logo" src="../assets/logo.jpg" />
        </a>
        <Nuxt-link to="/login" />
            <a
              class="nav-link active styling__nav__link"
              href=""
              target="_blank"
              >Home</a>
            <a class="nav-link styling__nav__link" href="" target="_blank"
              >Pricing</a
            >
            <b-nav-item>Docs</b-nav-item>
            <b-nav-item>Resources</b-nav-item>
            <a class="nav-link styling__nav__link" href="">Contact Us</a>
            <Nuxt-link to="/login" class="btn btn-warning"
              >Login <i class="fa fa-sign-in" aria-hidden="true"></i
            ></Nuxt-link>
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
            <h5 class="card-title">Feature One</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
            <a href="#" class="btn btn-warning">Go somewhere</a>
          </div>
        </div>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <div class="card mb-4 mx-auto">
          <div class="card-body">
            <h5 class="card-title">Feature Two</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
            <a href="#" class="btn btn-warning">Go somewhere</a>
          </div>
        </div>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <div class="card mb-4 mx-auto">
          <div class="card-body">
            <h5 class="card-title">Feature Three</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
            <a href="#" class="btn btn-warning">Go somewhere</a>
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
.nav {
  padding-left: 2% !important;
  padding-right: 2% !important;
}
.navbar-brand {
  width: 100px;
  height: 50px;
}

.navbar-logo {
  padding: 5px;
  height: 5%;
  width: 5%;
}

.nav-link{
  color: #000000;
  align-items: right;
  
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

.card {
  margin-right: 3rem;
}
</style>