<template>
  <div class="burger" @click="show = !show">
    <div></div>
    <div></div>
    <div></div>
  </div>
  <nav class="menu__body" v-if="show">
    <!-- <div class="menu__list">
      <router-link to="/">Home</router-link>
      <router-link to="/">About us</router-link>
      <router-link to="/">Menu</router-link>
      <router-link to="/">Features</router-link>
      <router-link to="/">Contact us</router-link>
      <button type="button" class="btn btn__auth">Log in</button>
      <button type="button" class="btn btn__auth btn-out">Log out</button>
    </div> -->
    <Navbar></Navbar>
  </nav>
</template>
<script>
// eslint-disable-next-line no-unused-vars
import Navbar from './NavBar.vue';
export default {
  name: "Burger",
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Navbar
  },
  data() {
    return {
      show: false
    }
  }
}
</script>
<style lang="scss">
$color_white: #ffffff;
$color_primary: #DC780B;
$color_main: #150C01;

.burger {
  width: 35px;
  height: 20px;
  position: relative;
  left: 15px;
  top: 20px;
  cursor: pointer;
  transition: transform .3s ease;
  z-index: 1000;

  &:hover,
  &:focus,
  &:active {
    transform: scaleY(1.4);
  }

  & div {
    content: '';
    position: absolute;
    height: 2px;
    width: 100%;
    border: 2px solid #000;
    left: 0;
    top: calc(50% - 1px);
    &:first-child {
      top: 0;
    }
    &:last-child {
      top: calc(100% - 2px);
    }
  }
}
.menu__body {
  position: absolute;
  z-index: 999;
  top: 0;
  left: 0;
  background: #000;
  width: 400px;
  height: 100%;
  opacity: 0.7;
  
}
.menu__list {
  margin: 0 auto;
  padding-top: 35%;
  display: flex;
  flex-direction: column;
  align-items: center;
  & a {
    color: $color_white;
    margin-bottom: 15px;
    text-decoration: none;
  }
}
@media (min-width: 700px){
  .burger {
    display: none;
  }
}
</style>