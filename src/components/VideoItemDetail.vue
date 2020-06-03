<template>
  <div class="my-4">
    <h3>{{videoItem.snippet.title}}</h3>
    <div class="embed-responsive embed-responsive-16by9 mb-4">
        <iframe class="embed-responsive-item" 
        :src="videoUrl" 
        allowfullscreen>
        </iframe>
        
    </div>
    <hr/>
  </div>
</template>

<script>
export default {
name : 'VideoItemDetail',
props : {
    videoItem : Object,
},
computed : {
    videoUrl () {
        // return this.videoItem.snippet.thumbnails.default.url
        return `https://youtube.com/embed/${this.videoItem.id.videoId}`
    }
}
}
</script>

<style>

</style>