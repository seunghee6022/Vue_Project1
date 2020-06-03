<template>
  <div>
  <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">{{movieItem.title}}</h5>
          
        
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <img :src="movieItem.backdrop_url" class="w-100" alt="movie poster image">
          <button class="btn btn-success my-2">
            Rating {{movieItem.user_rating}}</button>
          <p class="m-3">{{movieItem.overview}}</p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-success" data-dismiss="modal">Close</button>
    
        </div>
      </div>
    </div>
</div>  
  
  </div>
</template>

<script>
export default {
name : 'MovieListItemModal',
props : {
  movieItem : Object,
}
}
</script>

<style>

</style>