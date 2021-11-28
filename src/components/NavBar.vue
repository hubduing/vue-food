<template>
  <nav class="nav">
    <ul class="nav__items">
      <li class="nav__image">
        <router-link to="/">
          <img src="../img/logo.png" alt="logo">
        </router-link>
      </li>
      <!-- <li class="nav__link" v-for="item in menuList" :key="item.id">
        <router-link to="/">{{ item.title }}</router-link>
      </li> -->
      <li class="nav__link">
        <router-link to="/">Home</router-link>
      </li>
      <li class="nav__link">
        <router-link to="/about">About</router-link>
      </li>
      <li class="nav__link">
        <router-link to="/menu">Menu</router-link>
      </li>
      <li class="nav__link">
        <router-link to="/features">Features</router-link>
      </li>
      <li class="nav__link">
        <router-link to="/contact">Contact us</router-link>
      </li>
    </ul>
    <div class="auth-box">
      <button 
        type="button" 
        class="btn btn__auth" 
        @click="showBtn" 
        v-show="isShowBtn"
      >Log in</button>
      <button 
        type="button" 
        class="btn btn__auth btn-out" 
        @click="showBtnOut"
        v-show="isShowBtnOut"
      >Log out</button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isShowBtn: true,
      isShowBtnOut: false
    }
  },
  methods: {
    logOut() {
      localStorage.clear();
      this.$router.push("/login");
    },
    showBtn() {
      this.isShowBtn = !this.isShowBtn;
      this.isShowBtnOut = !this.isShowBtnOut;
    },
    showBtnOut() {
      this.isShowBtnOut = !this.isShowBtnOut;
      this.isShowBtn = !this.isShowBtn;
    }
  },
};
</script>
<style lang="scss">
$color_white: #ffffff;
$color_primary: #DC780B;
$color_main: #150C01;
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 30px;
}
.nav__items {
  display: flex;
  align-items: center;
  margin: 0;
}
.nav__image {
  margin-right: 35px;
}
.nav__link {
  margin-right: 40px;
  &:last-child {
    margin: 0;
  }
  & a {
    color: $color_main;
    opacity: 0.6;
    text-decoration: none;
    &:active,
    &:hover,
    &:focus {
      color: $color_primary;
    }
  }
}
.btn__auth {
  background: $color_primary;
  color: $color_white;
}
.btn-out {
}
@media (max-width: 700px){
  .nav {
    display: none;  
  }
}
</style>
