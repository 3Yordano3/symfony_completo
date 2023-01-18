<template>
  <div class="">
    <div class="grid-div mt-3" id="blockGrid">
      <div class="element" v-for="photo in tabPhotos" :key="photo" @click="livebox" >
        <div>
          <img :src="photo.url" alt="">
        </div>
        <div>
          <p class="text-center p-3">{{photo.text}}</p>
        </div>
      </div>
    </div>
  </div>
  <div class="anotherclass hideBlock mt-3" id="blockLivebox" style="position:relative">
    <img class="mt-10 mb-10 animate__animated" id="img-livebox" :src="photoSola" alt="">
    <button class="btn-close" @click="showPhotos">X</button>
  </div>
</template>

<script>

export default {
  name: "grid",
  props: {
    tabPhotos: {
      type: Array,
      default: null,
    },
  },
  // components:{LightBox}
  methods:{
    livebox(event){
      const blockGrid = document.getElementById("blockGrid");
      const blockLivebox = document.getElementById("blockLivebox");
      const imglivebox = document.getElementById("img-livebox");

      blockGrid.classList.add("hideBlock");
      blockLivebox.classList.remove("hideBlock");

      blockLivebox.classList.remove("animate__bounceOutDown");
      imglivebox.classList.add("animate__fadeIn");
      this.photoSola = event.path[0].currentSrc;
      console.log(blockGrid);
      console.log(blockLivebox);
    },
    showPhotos(event){
      console.log(event);
      const blockGrid = document.getElementById("blockGrid");
      const blockLivebox = document.getElementById("blockLivebox");
      const imglivebox = document.getElementById("img-livebox");

      imglivebox.classList.remove("animate__fadeIn");
      blockLivebox.classList.add("animate__bounceOutDown");

      blockGrid.classList.remove("hideBlock");
      blockLivebox.classList.add("hideBlock");
      blockLivebox.style.background = "rgba(0,0,0,0.8)";
    }
  },
  data(){
    return{
      photoSola : null,
    }
  }
}
</script>

<style lang="scss">

.grid-div{
  display: grid;
  width: 100%;
  height: auto;
  grid-template-columns: repeat(3,25%);
  grid-template-rows: 1fr;
  column-gap: 1%;
  row-gap: 30px;
  justify-content: center;
}

.element{
  width: 100%;
  padding:20px;
  background-color: white;
}

.element:hover{
  box-shadow: 15px 15px 18px rgba(0,0,0,.1);
  background-color: white;
  border: 0.2px solid rgba(0,0,0,.1);
  cursor:pointer;
  transition: all 300ms linear;
}

.anotherclass{
  display: grid;
  width: 100%;
  height: auto;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr;
  justify-content: center;
  justify-items: center;
  background-color: rgba(0,0,0,0.8);
}

.anotherclass img{
  width: 60%;
  height: auto;
  max-width: 100%;
  max-height: calc(100vh - 90px);
}

.hideBlock{
  display: none;
}

.btn-close{
  background-color: rgb(185, 28, 29);
  color:white;
  padding: 8px 10px;
  position: absolute;
  right:390px;
  top:50px;
  border-radius: 10px;
}
</style>