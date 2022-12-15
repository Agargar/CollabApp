<template>
  <div id="app">
    <top-header></top-header>
   <!-- <nav>
      <router-link to="/">Home</router-link> 
      <router-link to="/about">About</router-link>
    </nav>-->
    <router-view/>

    <body class="d-flex flex-column">
  
  <footer id="sticky-footer" class="flex-shrink-0 py-4 bg-dark text-white-50">
    <div class="container text-center">
      <small>Copyright &copy; Your Website</small>
    </div>
  </footer>
</body>
    
  </div>

</template>


<script>
import TopHeader from '@/components/TopHeader.vue';




  export default{
    components : {
      "top-header" : TopHeader,
      
    
      
    }

  }
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

h2 {
  text-align: left;
  font-weight: bold;
  padding: 50px;
  
  
}
html,
body {
  height: 100%;
}

#page-content {
  flex: 1 0 auto;
}

/* Other Classes for Page Styling */

body {
  background: #f5f3f3;
  /*background: linear-gradient(to right, #e8e7e3, #fff7fd);*/
}

footer{
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
}
</style>
