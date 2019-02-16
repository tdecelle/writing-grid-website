<template>
  <div id="app">
    <ul id="nav">
      <li class="nav_left"><router-link to="/">Writing Grid</router-link></li>
      <li class="nav_right"><router-link to="/listings">Listings</router-link></li>
      <li class="nav_right"><router-link to="/blog">Blog</router-link></li>
      <li class="nav_right"><router-link to="/login">Login</router-link></li>
    </ul>
    <router-view/>
  </div>
</template>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  #nav {
    padding: 0px;
    list-style-type: none;
    margin: 0;
    overflow: hidden;
    background-color: #4286f4;
  }

  #nav a {
    font-weight: bold;
    padding: 30px;
    font-size: 20;
    display: block;
    color: white;
    text-align: center;
    text-decoration: none;
  }
  
  .nav_left {
    float:left;
  }
  
  .nav_right{
    float:right;
  }
  
  #nav a:hover {
    background-color: #3e53a5;
  }

  #nav a.router-link-exact-active {
    background-color: #4fc14d;
  }
</style>
