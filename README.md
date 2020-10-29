# 0603 Vue Project
> Vue 영화 추천 & 검색 사이트 프로젝트

### 구현 과정

0. 최상단 App.vue에 MovieView와 VideoView import, 두 SFA를 Navbar에 연결

* MovieView

1. MovieView에 MovieList를 import하고, 버튼을 만든 뒤 누르면  axios를 통해 영화 정보를 가져와 props로 넘겨준다. 

   * 버튼 누르면 사라지는 기능 : 버튼누르면  `event.target.hidden=true` 실행되게 함

2. MovieList에서는 받은 영화 정보들을 row로 배치하고, v-for와 props로 MovieListItem에 보낸다.

   ```vue
     <MovieListItem v-for="movieItem in movieItems" 
         :key="movieItem.id"
         :movieItem="movieItem"
         />
   ```

   

3. MovieListItem에서 받은 개별 영화 정보들을 카드로 띄운 후, 카드의 버튼은 모달의 버튼으로 한다.

4. MovieListItemModal에서는 MovieListItem에서 받은 개별 영화 정보를 모달에 넣는다.

* VideoView

1. VideoView에 VideoSearch와 VideoItem를 연결한다.

2. VideoSearch에서 input값으로 검색할 키워드를 받아서 VideoView에 emit으로 보낸다.

3. VideoView에서 VideoSearch에서 받은 키워드로 검색한 후 결과를 VideoItem로 보낸다.

4. VideoItem에서는 받은 영화 정보들을 각각  VideoItemDetail로 보내는데

   ```vue
     <VideoItemDetail v-for="videoItem in videoItems"
         :key="videoItem.etag" 
         :videoItem="videoItem"/>
   ```

   v-for와 props로 바로 보낸다.

5. VideoItemDetail에서 동영상과 제목을 보여준다.



---

### 페어프로그래밍에서 느낀점

* 팀원과의 친밀도가 소통에 영향을 미치고 전체적인 결과에도 영향을 주는 것 같다.

  => 팀원과의 교류와 소통이 중요

* 가르쳐 주는 과정에서 많이 배운다.

* 막혔을 때 함께 해결방법을 찾아보는 과정에서 더 빠른 해결책을 발견 or 도출하는 것 같다.
