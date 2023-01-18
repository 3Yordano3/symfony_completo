<template>
  <div className="portfolio-container">
    <titleCenter/>
    <grid :tabPhotos="tabPhotos"/>
  </div>
</template>
<script>
import titleCenter from "../Components/titleCenter"
import grid from "../Components/grid"
import {photos} from '../donnees/photos-grid-portfolio';


export default {
  name: 'Portfolio',
  components: {titleCenter, grid},
  data() {
    return {
      tabPhotos: photos,
    };
  },
}
</script>
<!-- le mot cle module va a servir pour mettre un code deriere les classes css pour ne pas avoir des problemes si on a plusieurs elements avec le meme nom de classe dans autres fichiers et qu'on veut pas qu'il ait les memes styles que ces de ce fichier-->
<style lang="scss">
.portfolio-container {
  background-color: rgb(249, 249, 249);
  margin-top: 80px;
}
</style>
