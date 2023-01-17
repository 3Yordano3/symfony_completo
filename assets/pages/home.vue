<template>
<div>
  <Banner/>
  <Form/>
</div>
</template>
<script>
import Form from "../components/Form"
import Banner from "../components/Banner"
export default {
  name: 'home',
  data() {
    return {};
  },
  components : {Banner,Form}
}
</script>