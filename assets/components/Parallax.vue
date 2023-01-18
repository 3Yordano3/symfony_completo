<template>
  <div class="parallax"></div>
</template>

<script>
export default {
  name: "Parallax"
}
</script>

<style>
  .parallax{
    background-image:url("../../public/images/carousel/h1-slider-img-1.jpeg");
    height:500px;
    background-attachment:fixed;
    background-position:center;
    background-repeat:no-repeat;
    background-size:cover;
  }
</style>