<template>
    <div>
        <h1>Posts</h1>
        <div class="card-group">
  <div class="card" v-for="post in APIData" :key="post.id">
    
    <div class="card-body">
      <h5 class="card-title">{{post.title}}</h5>
      <p class="card-text">{{post.content}}</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  
</div>
    </div>
</template>

<script>
import axios from 'axios'
// import {getAPI} from '@/axios-api'

    export default {
        name:'Posts',
        data(){
            return{
                APIData:[],
            }
        },
         mounted() {
      axios({
      method: "GET",
      url: "http://127.0.0.1:8000/posts/",
    })
      .then((response) => {
       
        if(response.data.status == true){
           this.APIData = response.data
        }
      })
      .catch((err) => {
        console.log(err);
      })
  }




    // created () {
    //     getAPI.get('/posts/',)  
    //       .then(response => {
    //        console.log('Post APi recieved')
    //        this.APIData = response.data
    //       })
    //       .catch(err =>{ 
    //           console.log(err)
    //       })
      

    // }
    }
    
</script>

<style scoped>

</style>