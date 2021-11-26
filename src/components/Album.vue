<template>
  

 <div class="album d-flex flex-column pt-3">
    <div class="image">
      <img :src="album.poster" alt="">
    </div>
    <h4 class="text-center pt-4">{{album.title}}</h4>
    <div class="info text-center pt-4">
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

@import '../assets/style/vars.scss';

  .album{    
    align-items: center;
    width: calc(100% / 5 - 40px);
    margin: 10px 20px;
    height: 380px;
    background-color: rgba(112, 112, 112, 0.2);
    border: 2px solid $primary-color;
    transition: all .5s;
    &:hover{
      cursor: pointer;
      border: 2px solid black;
      border-radius: 10px;
    }
    .image{
      width: 80%;
      img{
        width: 100%;
      }
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