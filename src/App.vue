<template>
<div id="app">

</div>
  
</template>

<script>


const snoowrap = require('snoowrap');

const r = new snoowrap({
  userAgent: 'Vivek-Shinde00',
  clientId: 'y0BuNnmycbQe-DLy3arWug',
  clientSecret: '	OHS7racZqCoShfAwACDGoEvREVX3kg',
  refreshToken: '1139991457823-xCSDimBNAOSyhpmZb_OKivQXvj7ISA',
  
  accessToken:'1139991457823-yFlBpY2OVCBsS_hZroHXHia9xUj05w',
 
});
r.config({ debug: true });
r.getHot().map(post => post.title).then(console.log);


</script>

<style scoped>


</style>
