<template>
  <div>
    <ul class="footer-list">
      <li class="footer-title"><a href="/" >{{ footersList.title }}</a></li>
      <li class="footer-item">Landingpage</li>
      <li class="footer-item">Documentation</li>
      <li class="footer-item">Referral Program</li>
      <li class="footer-item">UI & UX Design</li>
      <li class="footer-item">Web Design</li>
    </ul>
  </div>    
</template>
<script>
export default {
  name: "FooterList",
  props: ['footersList']
}
</script>
<style lang="scss">
$colorWhite: white;
.footer-list {
  display: flex;
  flex-direction: column;
  max-width: 262px;
  text-align: left;
}
.footer-item {
 display: inline-block;
  font-size: 14px;
  line-height: 16px;
  margin-bottom: 20px;
  opacity: 0.7;
  color: $colorWhite;
}
.footer-title { 
  margin-bottom: 20px;
  opacity: 1;
  & a {
    font-family: 'Philosopher', sans-serif;
    font-weight: 700;
    font-size: 18px;
    line-height: 20px;
    text-transform: uppercase;
    color: $colorWhite;
  }
}
</style>