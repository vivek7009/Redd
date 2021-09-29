

<template>
  
    <div id="app">
      <div class="container">
      <div class="card-columns">
      <div class="card p-3 ">

          <blockquote class="card-blockquote ">
 
            <p>reddit's awesome and all, but you may have a bit of a
            problem. we've seen far too many requests come from your ip address
              recently.</p>
          </blockquote>
      </div>
    </div>

      <div v-show="r.getHot().map(post => post.title).then(console.log)" >
        
            Loading...
     
        
      </div>
    </div>
  
  </div>
  

</template>

<script>
  const snoowrap = require('snoowrap');
    
 const r = new snoowrap({
  userAgent: 'Vivek-Shinde00',
  clientId: 'y0BuNnmycbQe-DLy3arWug',
  clientSecret: 'OHS7racZqCoShfAwACDGoEvREVX3kg',
  refreshToken: '1139991457823-xCSDimBNAOSyhpmZb_OKivQXvj7ISA',
  accessToken:'1139991457823-yFlBpY2OVCBsS_hZroHXHia9xUj05w',
 });
r.config({ debug: true });

 // Submitting a link to a subreddit
r.getSubreddit('gifs').submitLink({
  title: 'Mt. John',
  url: 'https://i.imgur.com/n5iOc72.gifv'
});

// Printing a list of the titles on the front page
r.getHot().map(post => post.title).then(console.log);
r.getSubreddit('Akash').then(console.log);

 
</script>

<style scoped>


</style>
