<template>
  <div class="wrapper">
    <div class="content">
      <section class="features">
        <h3 class="title features__title">Features</h3>
        <p class="subtitle features__subtitle">Food with a New Passion</p>

        <div class="features__box">
          <div class="features__box-content" v-for="item in foods" :key="item.id">
            <div class="_img features__box-image">
              <img :src=item.nameImage alt="food">
            </div>
            <h4>{{ item.title }}</h4>
            <p>It can be a very secure path to earn good money and make you very successful creative entrepreneur.</p>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Features',
  data() {
    return {
      foods: [
        {title: 'Quality Food', id: 1, nameImage: require('../img/group1.png')}, 
        {title: 'Food Delivery', id: 2, nameImage: require('../img/group1.png')}, 
        {title: 'Super Taste', id: 3, nameImage: require('../img/group1.png')}
      ]
    }
  }
}
</script>

<style lang="scss">

.features {
  padding: 150px 0;
  margin-bottom: 100px;
  text-align: center;
  &__subtitle {
    margin-bottom: 44px;
  }
  &__box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: center;
    & h4 {
      margin-bottom: 15px;
    }
  }
  &__box-content {
    margin-right: 90px;
    flex-direction: column;
    &:last-child {
      margin-right: 0;
    }
  }
  &__box-image {
    width: 88px;
    height: 88px;
    margin: 0 auto 33px;
    & img {
      object-fit: fill;
    }
  }
}
@media (max-width: 1000px) {
  .features__box {
    flex-wrap: wrap;
  }
  .features__box-content {
    margin-right: 10px;
    max-width: 48%;
    justify-content: space-evenly;
    margin-bottom: 15px;
  }
}
@media (max-width: 668px) {
  .features__box-content {
    margin-right: 10px;
    max-width: 100%;
    justify-content: space-evenly;
  }
}
</style>
