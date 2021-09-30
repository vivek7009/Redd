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

const snoowrap = require('snoowrap');
const r = new snoowrap ({
  userAgent: 'Vivek-Shinde00',
  clientId: 'y0BuNnmycbQe-DLy3arWug',
  clientSecret: '	OHS7racZqCoShfAwACDGoEvREVX3kg',
  refreshToken: '1139991457823-xCSDimBNAOSyhpmZb_OKivQXvj7ISA',
  
  accessToken:'1139991457823-yFlBpY2OVCBsS_hZroHXHia9xUj05w',
 
});
r.getHot().map(post => post.title).then(console.log);

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
           

            
            console.log(snoowrap);
            r.getHot().map(post => post.title).then(console.log);
           

          }
      }
  }
</script>
<style>
</style>
