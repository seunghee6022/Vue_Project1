<template>
  <div class="container my-4">
    <h1>나만의 무비 컬렉션</h1>
    <button class="btn btn-primary" @click="getMovieList">영화 가져오기</button>
    <MovieList :movieItems="movieItems"/>
  </div>
</template>

<script>
import axios from 'axios'
import MovieList from '../components/MovieList.vue'
export default {
name : 'MovieView',
components:{
  MovieList,
},
data () {
  return{
    movieItems : {},
  }
  
},
methods : {
  getMovieList (event) {
    axios.get('http://www.json-generator.com/api/json/get/ceNyuXZmwi?indent=2')
    .then(res => {
      console.log("영화를 가져옵니다.")
      // console.log(event.target.hidden)
      event.target.hidden = true
      this.movieItems = res.data
      
    })
    .catch(err => console.error(err))
  }
}
}
</script>

<style>

</style>
