<template>
  <div class=" d-flex align-items-center mx-3">
    <select 
      class="form-select" 
      v-model="genreSelection" 
      @change="$emit('sendValue',genreSelection)"
    >
      <option value="selected">Seleziona un genere</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  data(){
    return{
      genreSelection: 'selected'
    }
  }
}
</script>

<style>

</style>