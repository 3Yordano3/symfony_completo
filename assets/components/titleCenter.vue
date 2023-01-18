<template>
    <div>
      <h1 class="portfolio-title text-4xl mt-4">PortFolio</h1>
    </div>
</template>

<script>
export default {
  name: 'titleCenter',
  data() {
    return {};
  },
}
</script>

<!-- le mot cle module va a servir pour mettre un code deriere les classes css pour ne pas avoir des problemes si on a plusieurs elements avec le meme nom de classe dans autres fichiers et qu'on veut pas qu'il ait les memes styles que ces de ce fichier-->
<style>
.portfolio-title{
  text-align: center;
}
</style>
