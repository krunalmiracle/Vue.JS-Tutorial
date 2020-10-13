<template>
  <div class="Tweet">
    <h2 class="tweet_inline">{{name}}: </h2>
    <p class="tweet_inline">{{message}}</p>
  </div>
</template>

<script>
export default {
  name: 'Tweet',
  props: {
    message: String,
    name:String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px 0 0;
}
.Tweet{
    color: black;
    background-color: whitesmoke;
    border-style: solid;
    border-color: cyan;
    border-width: 5px;
}
.tweet_inline{
    column-width: auto;
    display: inline; 
    font-size: 30px;
}
</style>
