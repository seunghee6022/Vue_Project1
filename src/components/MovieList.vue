<template>
  <div class="row mt-3">
      <MovieListItem 
      v-for="movieItem in movieItems" 
      :key="movieItem.id"
      :movieItem="movieItem"
      />
  </div>
</template>

<script>
import MovieListItem from './MovieListItem.vue'

export default {
name : 'MovieList',
components:{
    MovieListItem,
},
props :{
    movieItems : Array,
}
}
</script>

<style>

</style>