<template>
  <div class="app">
    <div class="wrapper">
      <div class="content">
        <!-- <nav-bar v-if="!$route.fullPath.includes('login')"></nav-bar> -->
        <nav-bar></nav-bar>
        <burger-menu></burger-menu>
      </div>
    </div>
    <router-view></router-view>
    <footer-component></footer-component>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import BurgerMenu from './components/Burger.vue'
import FooterComponent from './components/Footer.vue'
import './Normalize.css'
import './UI.scss'
export default {
  name: "App",
  components: {
    NavBar,
    BurgerMenu,
    FooterComponent
  },
  // methods: {
  //     logOut() {
  //     localStorage.clear();
  //     this.$router.push("/login");
  //   },
  // }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;0,700;0,900;1,300;1,400;1,500;1,700;1,900&display=swap');
.navbar {
  padding: 30px;
}

</style>
