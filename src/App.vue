<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-dark">
       <a class="navbar-brand" href="#"><router-link class="text-decoration-none text-white click" to="/">Movie App</router-link></a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="navbar-item text-decoration-none" href="#"><router-link class="text-decoration-none text-white click" to="/">Movie</router-link></a>
      </li>
      <li class="nav-item active mx-3">
        <a class="navbar-item text-decoration-none" href="#"><router-link class="text-decoration-none text-white click" to="/video">Video</router-link></a>
      </li>
      </ul>
  </div>
</nav>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
.click :hover{
  color :#42b983
}
</style>
