<template>
  
  <div id="app">
    <div class="container">
      <div class="card-columns">

        <div class="card p-3"
          v-for="post in posts" :key="post.id">

          

        </div>

      </div>

      <div class="text-center"
        v-show="postsLoading">
         Loading...
      </div>
    </div>
  </div>
</template>


<script> 

  export default {
      created () {
        this.getPosts()
      },
      data () {
        return {
          posts: [],
          postsLoading: false,
          
        }
      },
      methods: {
          getPosts () {
            var myArr = ["Orange", "Banana", "Mango", "Kiwi" ];
            console.log(myArr);

          }
      }
  }
</script>
<style>
</style>
