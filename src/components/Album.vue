<template>
  

 <div class="album">
    <img :src="album.poster" alt="">
    <h4 class="text-center">{{album.title}}</h4>
    <div class="info text-center ">
      <p>{{album.author}}</p>
      <p>{{album.year}}</p>
    </div>
  </div>


</template>

<script>
export default {
  name: 'Album',
  props:{
    album: Object
  }
}
</script>

<style lang="scss">
  .album{
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    width: calc(100% / 5 - 40px);
    margin: 20px;
    height: 380px;
    background-color: rgba(112, 112, 112, 0.2);
    img{
      width: 90%;
      height: 40%;
    }
    h4{
      text-transform: uppercase;
    }
    .info{
      line-height: 0px;
      color: rgba(211, 211, 211, 0.404);
    }
  }
</style>