<template>
  <section class="contact">
    <div class="wrap">
      <h3 class="title contact__title">Contact</h3>  
      <h4 class="subtitle contact__subtitle">Food Stalls with Persons but also specialized equipment, Skills to manage.</h4>
      <form action="" method="post" class="form">
        <input type="text" name="contact-input" placeholder="Enter your message" class="input">
        <button type="submit" class="btn btn-contact">Send</button>
      </form>
    </div>
  </section>
</template>
<script>
export default {
  name: "Contact"
}
</script>
<style lang="scss">
.contact {
  padding: 150px 0;
  background: rgba(220,120,11, 0.1);
  min-width: 100vw;
}
.wrap {
  max-width: 750px;
  padding: 115px 30px;
  margin: 0 auto;
}
.contact__title,
.contact__subtitle {
  text-align: center;
}
.form {
  display: flex;
  margin: 0 auto;
  align-items: center;
}
.input {
  flex: 1;
  font-size: 16px;
  line-height: 41px;
  padding: 19px;
  color: #000000;
  opacity: 0.5;
  background: #FFFFFF;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
  border: none;
}
.btn-contact {
  padding: 30px 57px;
  color: #ffffff;
  background: #DC780B;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}
@media (max-width: 450px){
  .wrap {
    padding: 50px 30px;
  }
  .form {
    display: flex;
    flex-direction: column;
    & input {
      margin-bottom: 15px;
    }
  }
}
</style>