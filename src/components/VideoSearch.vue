<template>
  <div>
    <input class="w-50" style="height:2rem" type="text" @keypress.enter="searchVideo(search)" v-model="search">
    <button class="btn btn-success" @click="searchVideo(search)">검색</button>
  </div>
</template>

<script>
export default {
name : 'VideoSearch',
data () {
    return {
        search : '',
    }
},
methods : {
    searchVideo(search) {
        console.log("VS:",search)
        this.$emit('movie-search', search)
    }
}
}
</script>

<style>

</style>