<template>
  <div class="d-flex flex-wrap">
    <Album 
     v-for="(album,index) in albumArray"
     :key="index"
     :album='album'
    />
  </div>  
</template>

<script>

import axios from 'axios';
import Album from './Album.vue';

export default {
 name: 'AlbumsRow',
 components:{
   Album
 },
 data(){
   return{
     albumArray: [],
     apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music'
   }
 },
 methods:{
   getApi(){
     axios.get(this.apiUrl)
      .then(r => {
        //console.log(r);
        this.albumArray = r.data.response;
        console.log(this.albumArray);
      })
      .catch(e => {
        console.log(e);
      })
   }
 },
 mounted(){
   this.getApi();
 }
}
</script>

<style lang="scss" scoped>
  
</style>