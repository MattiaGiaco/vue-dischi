<template>
  <div class="main-wrapper">
    <header>
      <img class="my-1 mx-3" src="./assets/img/spotify-logo.png" alt="">
    </header>

    <div class="container mt-5">
      <AlbumsRow />
    </div>
  </div>
</template>

<script>

import AlbumsRow from './components/AlbumsRow.vue';

export default {
  name: 'App',
  components: {
    AlbumsRow
  }
}
</script>

<style lang="scss">

@import './assets/style/vars.scss';
@import './assets/style/generals.scss';

.main-wrapper{
  min-height: 100vh;
  background-color: $primary-color;
  header{
    height: 60px;
    background-color: rgba(112, 112, 112, 0.2);
    img{
      width: 50px
    }
  }
}

</style>
