<template>
  <div class="wrapper">
    <div class="content">
      <section class="menu">
        <h3 class="title menu__title">Menu</h3>
        <h4 class="subtitle menu__subtitle">Food Full of treaty Love</h4>
        <p class="text menu__text">There are many things are needed to start the Fast Food Business. You need not only Just Food Stalls with Persons but also specialized equipment, Skills to manage Customers, </p>
        <div class="carts">
          <div class="cart" v-for="elem in menuFood" :key="elem.id">
            <div class="_img cart__image">
              <img :src="elem.src" alt="Vegie Muffen">
            </div>
            <div class="info">
              <div class="info-box">
                <h2 class="info__title">{{ elem.title }}</h2>
                <h2 class="info__price">{{ elem.price }}$</h2>
              </div>
              <p class="info__description">
                There are many things are needed to start the Fast Food Business.
              </p>
              <div class="cart__box">
              <button type="button" class="btn cart__btn">&#43;</button>
              <Rating></Rating>
              </div>
            </div>            
          </div>
        </div>
        <!-- <button class="btn btn-more">Learn More</button> -->
      </section>
    </div>
  </div>
</template>

<script>
import Rating from '../components/Rating.vue'
export default {
  components: { Rating },
  name: 'Menu',
  data() {
    return {
      menuFood: [
        {title: 'Vegie Muffen', id: 1, price: 16, src: require('../img/carts/food1.png')},
        {title: 'Salads', id: 2, price: 12, src: require('../img/carts/food2.png')},
        {title: 'Burger', id: 3, price: 10, src: require('../img/carts/food3.png')},
        {title: 'Delmonico Steak dish', id: 4, price: 14, src: require('../img/carts/food4.png')},
        {title: 'Egg Masala', id: 5, price: 9, src: require('../img/carts/food5.png')},
        {title: 'Peach Melba dish', id: 6, price: 15, src: require('../img/carts/food6.png')},
      ]
    }
  },
}
</script>

<style lang="scss">
.menu {
  display: flex;
  flex-direction: column;
  padding: 150px 0;
  &__title,
  &__subtitle {
    text-align: center;
  }
  &__subtitle {
    margin-bottom: 25px;
  }
  &__text {
    text-align: center;
    margin-bottom: 21px;
    max-width: 70%;
    margin: 0 auto;
  }
}
.carts {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 40px;
  row-gap: 30px;
  padding-top: 60px;
  padding-bottom: 50px;
}
.cart {
  border: 1px solid rgba(0, 0, 0, 0.1);
  box-sizing: border-box;
  border-radius: 75px 10px 10px 10px;
  &__image {
    min-width: 360px;
    min-height: 264px;
  }
  &__box {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__btn {
    background: #DC780B;
    padding: 11px 18px;
    color: #fff;
  }
}
.info {
  display: flex;
  flex-direction: column;
  padding: 0 25px 25px;
  &-box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
    padding-bottom: 20px;
  }
  &__description {
    padding-bottom: 20px;
  }
}
.btn-more {
  text-align: center;
  text-decoration: none;
  padding: 11px 30px 12px;
  background: inherit;
  color: #DC780B;
  border: 1px solid #000;
  margin: 0 auto;
}
</style>
