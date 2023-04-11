<template>
<div>
<!--  <Banner/>-->
<!--  <Form/>-->
  <Carousel/>
  <Parallax/>
</div>
</template>
<script>
// import Form from "../components/Form"
// import Banner from "../components/Banner"
import Carousel from "../components/Carousel"
import Parallax from "../components/Parallax"
export default {
  name: 'home',
  data() {
    return {};
  },
  components : {Carousel,Parallax}
}
</script>

<style>
.nav-transparent a{
  color: white;
}
</style>