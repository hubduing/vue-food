<template>
  <div class="home">
    <banner></banner>
    <market></market>
    <rating></rating>
  </div>
</template>

<script>
// @ is an alias to /src
import Banner from '../components/Banner.vue';
import Market from '../components/Market.vue';
import Rating from '../components/Rating.vue';
export default {
  name: 'Home',
  components: {
    Banner,
    Market,
    Rating
  }
}
</script>
