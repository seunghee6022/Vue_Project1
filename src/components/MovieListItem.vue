<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
      <div class="card" style="width: 18rem;">
        <img :src="movieItem.poster_url" class="card-img-top" alt="movie poster image">
        <div class="card-body">
            <h5 class="card-title">{{movieItem.title}}</h5>
            <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
                영화 정보 상세보기
            </button>
             </div>
        </div>
    <MovieListItemModal :movieItem="movieItem"/>
  </div>
</template>

<script>
import MovieListItemModal from './MovieListItemModal.vue'
export default {
name : 'MovieListItem',
components:{
    MovieListItemModal,
},
props : {
    movieItem : Object,
    
},
methods : {
}
}
</script>

<style>

</style>