<template>
  <div class="mt-3">
    <h1 class="m-3">영화 예고편 검색</h1>
    <VideoSearch @movie-search="searchVideo"/>
    <VideoItem :videoItems="videoItems"/>
  </div>
</template>

<script>
import axios from 'axios'
import VideoSearch from '@/components/VideoSearch.vue'
import VideoItem from '@/components/VideoItem.vue'

const API_KEY = process.env.VUE_APP_API_KEY
const API_URL = 'https://www.googleapis.com/youtube/v3/search'
export default {
  name: 'VideoView',
  components: {
    VideoSearch,
    VideoItem
  },
  data () {
    return {
      videoItems : [],
    }
  },
  methods : {
    searchVideo (search) {
      axios.get(API_URL, {
        params : {
          key : API_KEY,
          part : 'snippet',
          type : 'video',
          q : search+' trailer',
        }
      })
    .then(res => {
      res.data.items.forEach(item => {
        const parser = new DOMParser()
        const doc = parser.parseFromString(item.snippet.title, 'text/html')
        item.snippet.title = doc.body.innerText
      })
      console.log(res.data.items)
      this.videoItems = res.data.items
      // this.$emit('result',res.data.items)
    })
    .catch(err => console.error(err))
    }
  }
}
</script>
