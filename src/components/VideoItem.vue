<template>
  <div>
      <VideoItemDetail v-for="videoItem in videoItems"
      :key="videoItem.etag" 
      :videoItem="videoItem"/>
  </div>
</template>

<script>
import VideoItemDetail from './VideoItemDetail.vue'
export default {
name : 'VideoItem',
components : {
    VideoItemDetail,
},
props : {
    videoItems : Array,
},

}

</script>

<style>

</style>