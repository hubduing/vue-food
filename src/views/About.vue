<template>
  <div class="wrapper">
    <div class="content">
      <section class="about">
        <div class="about__box">
          <div class="_img about__image">
            <img src="../img/about.png" alt="about">
          </div>
          <div class="text-block">
            <h3 class="title about__title">About us</h3>
            <h4 class="subtitle about__subtitle">Food Stalls with Persons but  to  Product marketing plane catlogues etc to. </h4>
            <p class="text about__text">There are many things are needed to start the Fast Food Business. You need not only Just Food Stalls with Persons but also 
equipment  make your marketing plane Effective.</p>
            <button type="button" class="btn btn-about">Read More</button>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "About"
}
</script>

<style lang="scss">
.btn-about {
  color: #FFFFFF;
  padding: 11px 34px 12px 30px;
  background: #DC780B;
}
.about {
  padding: 150px 0;
  &__box {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__image {
    width: 50%;
    height: 300px;
    margin-right: 10%;
    & img {
      object-fit: cover;
    }
  }
  &__title {
    margin-bottom: 10px;
  }
  &__subtitle {
    margin-bottom: 30px;
  }
  &__text {
    margin-bottom: 30px;
  }
}
.text-block {
  flex-direction: column;
  text-align: left;
}
@media (max-width: 700px) {
  .about__box {
      display: block;
  }
  .about__image {
    width: 100%;
    margin-bottom: 15px;
  }
  .text-block {
      text-align: center;
  }
}
</style>