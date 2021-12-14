<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-secondary fixed-top">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
          <router-link class="nav-link active" aria-current="page" :to="{ name:'Home'}">Home</router-link> 
          <router-link class="nav-link" :to="{ name:'About'}">About</router-link>
          <router-link class="nav-link" :to="{ name:'Posts'}">Posts</router-link>
       
        
      </div>
    </div>
  </div>
</nav>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

</style>