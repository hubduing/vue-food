<template>
  <section class="market">
    <div class="wrapper">
      <div class="content market-df">
        <div class="store">
          <h3 class="title store__title">Take away</h3>  
          <h4 class="subtitle store__subtitle">Food Stalls with Persons but  to  Product marketing plane. </h4>
          <p class="text store__text">There are many things are needed to start the Fast Food Business. You need not only Just Food Stalls with Persons but also specialized equipmentwith Persons but also  Just Food Stalls with Persons.</p>
          <div class="store-link">
            <a href="https://www.apple.com/app-store/" @click.prevent class="btn btn-store">
              <span>Apple Store</span>
            </a>  
            <a href="https://play.google.com/store" @click.prevent class="btn btn-store">
              <span>Google Play</span>
            </a>  
          </div>
        </div>
        <div class="_img market__image">
          <img src="../img/phone.png" alt="phone">  
        </div>
      </div>      
    </div>      
  </section>
</template>
<script>
export default {
  name: "Market"
}

</script>
<style lang="scss">
$colorWhite: white;
$colorMainDark: #150C01;
.market-df {
  display: grid;
  grid-template-columns: 3fr 1fr;
}
.store {
  display: flex;
  flex-direction: column;
  padding: 114px 0 129px;
  &__text {
    margin-bottom: 54px;
  }
}
.btn-store {
  align-items: center;
  color: $colorWhite;
  padding: 15px 30px 14px 60px;
  background: $colorMainDark;
  transition: all .3s ease;
  margin-right: 30px;
  & span {
    position: relative;
  }
  & span::before {
    position: absolute;
    content: '';
    left: -32px;
    top: -4px;
    width: 24px;
    height: 26px;
  }
  &:first-child span::before {
    background-image: url(../img/apple.png);
  }
  &:last-child {
    margin-right: 0;
    & span::before {
      background-image: url(../img/google-play.png);
    }
  }
  &:focus,
  &:hover,
  &:active {
    border: 1.5px solid #E6E2DD;
    box-sizing: border-box;
    background: #FDF9F5;
    color: $colorMainDark
  }
}

@media (max-width: 768px) {
  .market__image {
    display: none;
  }
  .market-df {
      grid-template-columns: 1fr;
  }
}
@media (max-width: 450px) {
  .btn-store {
    padding: 5px 10px 5px 40px;
    margin-right: 5px;
  }
}
</style>