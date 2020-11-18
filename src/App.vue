<template>
  <div id="app">
    <h1 class="TitleTxt">TweetBox</h1>
    <Tweet v-for="msg in msgArr" name="John" :message="msg" :key="msg"/>
    <input v-model="inputTxt" type="text" class="chat_inline"> <!-- This input is realted to variable inputTxt-->
    <button v-on:click="clickAlert2()" class="chat_inline">Click Me </button>
  </div>
</template>

<script>
import Tweet from './components/Tweet.vue'

export default {
  name: 'App',
  components: {
    Tweet
  },
  data(){
    return{
      msgArr:["Well Hello There", "Patience my Friend"],
      inputTxt: ""
    }
  },
  methods:{
    clickAlert: function(){
      alert("Button Clicked!")
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 60px;
}
button{
  width: 120px;
  height: 40px;
}
.chat_inline{
  width: 250px;
    display: inline; 
    font-size: 30px;
}
.TitleTxt{
  font-size: 40px;
  text-align: center;
  color: black;
}
</style>
