<template>
  <div class="wrapper bg-footer">
    <div class="content">
      <footer class="footer">
        <ul class="info-company">
           <li>
             <div class="_img logo">
               <img src="../img/logo.png" alt="logo">
             </div>
           </li>
           <li><a href="https://yandex.ru/">www.companyname.com</a></li>
           <li><a href="mailto:companyname@gmail.com">companyname@gmail.com</a></li>
           <li><a href="tel:+74851180325">Phone: +7 485-118-03-25</a></li>
        </ul>
        <footer-list 
          :footersList="item"
          v-for="item in footersList" 
          :key="item.id">
        </footer-list>
      </footer>
    </div>
  </div>
</template>

<script>
import FooterList from './FooterList.vue'
export default {
  components: { FooterList },
  name: "Footer",
  data() {
    return {
      footersList: [
        {id: 1, title: "Home"},
        {id: 2, title: "Menu"},
        {id: 3, title: "Company"}
      ]
    }
  }
}
</script>

<style lang="scss">
$colorFooter: #252525;
$colorWhite: white;


.footer {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  padding: 135px 0 100px;
}
.bg-footer {
  background-color: $colorFooter;
  min-width: 100vw;
}
.logo {
  display: inline-block;
  width: 60px;
  height: 60px;
  margin-bottom: 17px;
}
.info-company {
  display: flex;
  flex-direction: column;

  & li {
    display: inline-block;
  }
  & a {
    display: inline-block;
    color: $colorWhite;
    opacity: 0.7;
    font-size: 14px;
    line-height: 16px;
    margin-bottom: 17px;
  }
}


@media (max-width: 768px) {
  .footer {
    grid-template-columns: repeat(2, 1fr);
    padding: 50px 0;
  }
}
@media (max-width: 550px) {
  .footer-list {
    display: none;
  }
  .footer {
    grid-template-columns: 1fr;
    padding: 25px 0;
  }
  .info-company {
    margin: 0 auto;
  }
}
</style>