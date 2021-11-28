<template>
  <div class="wrapper">
    <div class="wrapper__image">
      <div class="banner__image">
        <img src="../img/banner.png" alt="banner">
      </div>
    </div>
    <div class="content">
      <div class="banner">
        <h1 class="banner__title">Making time a good time by making food the good food.</h1>
        <p class="banner__text">There are many things are needed to start the Fast Food Business. You need not only Just Food Stalls with Persons but also specialized equipment,</p>
        <div class="banner-box">
          <button class="btn btn-banner">Order Now</button>
          <button class="btn btn-banner">Food Details</button>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'Banner',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.wrapper__image {
  position: absolute;
  right: 3px;
  top: 30px;
  z-index: -1;
}
.banner {
  padding-top: 160px;
  padding-bottom: 223px;
  // font-family: 'Philosopher', sans-serif;
  font-family: 'Roboto', sans-serif; 
  color: #150C01;
  max-width: 50%;
  &__title {
    font-size: 48.83px;
    line-height: 58px;
    font-weight: 700;
    font-family: 'Philosopher', sans-serif;
    margin-bottom: 42px;
  }
  &__text {
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    opacity: 0.7;
    margin-bottom: 50px;
  }
  &__image {
  position: relative;
  z-index: -1;
    & img {
      object-fit: fill;
      width: 801px;
      height: 670px;
    }
  }
}
.banner-box {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.btn {
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  border-radius: 5px;
  border: none;
}
.btn-banner {
  background: #DC780B;
  padding: 20px 40px;
  color: #fff;
  margin-right: 30px;
}

._img {
  position: relative;
  
  & img {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: fill;
  }
}

@media (max-width: 1200px) {
  .banner {
    padding-top: 100px;
    padding-bottom: 150px;
  }
  .banner__image img {
    max-width: 500px;
    max-height: 450px;
  }
}
@media (max-width: 900px) {
  .banner__image {
    display: none;
  }
  .banner {
    max-width: 100%;
    padding-top: 50px;
    padding-bottom: 50px;
  }
  .banner__text {
    font-size: 25px;
    line-height: 30px;
  }
}
</style>
